InteractionAPP/
├── app/
│   ├── main.py                   # 程序入口，初始化 DI 容器和 EventBus，然后启动 GUI
│   ├── models/
│   │   ├── __init__.py
│   │   ├── config.py             # ConfigScheme, ControllerDevice, Interaction, ActionMapping
│   │   └── ...                   
│   ├── services/
│   │   ├── __init__.py
│   │   ├── config_service.py     # ConfigManager 类
│   │   ├── live_service.py     # DouyinLiveWebFetcher 类（或改为 LiveFetcher）
│   │   ├── hardware_service.py   # 硬件驱动抽象与 SPI
│   │   └── task_service.py       # 任务调度（定时、条件触发）
│   ├── controllers/
│   │   ├── __init__.py
│   │   ├── main_controller.py    # 整体协调：菜单、子窗口打开
│   │   ├── config_controller.py  # 配置面板逻辑
│   │   ├── stream_controller.py  # 弹幕拉流启动/停止
│   │   ├── task_controller.py    # 任务窗逻辑
│   │   └── ...                  
│   ├── views/
│   │   ├── __init__.py
│   │   ├── gui_app.py            # DouyinMonitorApp
│   │   └── frames/               
│   │       ├── monitor_frame.py
│   │       ├── config_frame.py
│   │       ├── control_object_management_frame.py
│   │       ├── interaction_frame.py
│   │       ├── mapping_frame.py
│   │       └── import_export_frame.py
│   └── utils/
│       ├── __init__.py
│       ├── event_bus.py          # 发布-订阅总线
│       ├── logger.py             # 日志封装
│       └── async_helper.py       # asyncio 与 Tkinter 集成
├── configs/                      # 用户方案 JSON 文件
├── tests/                        # 单元测试
│   ├── test_config.py
│   ├── test_fetcher.py
│   └── ...
├── requirements.txt
└── README.md