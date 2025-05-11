### [👉👉👉♥♥点此进入♥观看入口👈👈👈](http://a.d44k.cc/mfwz.html)
<br></br><br></br><br></br>
def create_widgets(self):
        # 顶部框架 - 任务输入
        top_frame = ttk.LabelFrame(self.root, text="添加新任务", padding=10)
        top_frame.pack(pady=10, padx=10, fill="x")
        
        # 任务标题
        ttk.Label(top_frame, text="任务标题:").grid(row=0, column=0, sticky="w")
        self.title_entry = ttk.Entry(top_frame, width=40)
        self.title_entry.grid(row=0, column=1, padx=5, pady=5, sticky="ew")
        
        # 任务描述
        ttk.Label(top_frame, text="任务描述:").grid(row=1, column=0, sticky="w")
        self.desc_text = tk.Text(top_frame, height=3, width=40)
        self.desc_text.grid(row=1, column=1, padx=5, pady=5, sticky="ew")
        
        # 负责人
        ttk.Label(top_frame, text="负责人:").grid(row=2, column=0, sticky="w")
        self.owner_entry = ttk.Entry(top_frame, width=20)
        self.owner_entry.grid(row=2, column=1, padx=5, pady=5, sticky="w")
        
        # 截止日期
        ttk.Label(top_frame, text="截止日期:").grid(row=2, column=2, sticky="w")
        self.date_entry = ttk.Entry(top_frame, width=15)
        self.date_entry.grid(row=2, column=3, padx=5, pady=5, sticky="w")
        self.date_entry.insert(0, datetime.now().strftime("%Y-%m-%d"))
        
        # 优先级
        ttk.Label(top_frame, text="优先级:").grid(row=3, column=0, sticky="w")
        self.priority_var = tk.StringVar(value="中")
        priority_menu = ttk.Combobox(
            top_frame, 
            textvariable=self.priority_var, 
            values=["高", "中", "低"], 
            state="readonly", 
            width=10
        )
        priority_menu.grid(row=3, column=1, padx=5, pady=5, sticky="w")
