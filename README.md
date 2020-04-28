# deepdream
make deepdream image easily
class Deepdream(builtins.object)
 |  这是一个用来生成Deepdream图像的类
 |
 |  Methods defined here:
 |
 |  __init__(self)
 |      初始化函数，默认不使用多个卷积层
 |
 |  load_inception_model(self, layers_name)
 |      通过选定卷积层载入预训练模型
 |      :param layers_name:卷积层名称,若传入一个列表则打开多卷积层模式
 |      :return: 模型
 |
 |  make_nosie_image(self, height, width, channles, bias)
 |      生成噪点图像
 |      :param height: 生成图片长
 |      :param width: 生成图片宽
 |      :param channles: 生成图片通道数
 |      :param bias: 偏置项
 |      :return: 噪点图片
 |
 |  normalize_image(self, image)
 |      将输入图片进行标准化于，可用于图片的显示于保存
 |      :param image: 输入图片
 |      :return: 输出图片
 |
 |  octave_render(self, model, image, steps=100, setp_size=0.01, verbose=1, channels: list = [13], scale=1.3, octaves=range(-2, 3))
 |      绘制deepdream图像，octave模式
 |      :param model: 输入模型
 |      :param image: 输入图像
 |      :param steps: 训练轮次
 |      :param setp_size: 训练速率
 |      :param verbose: 训练进度显示模式1为显示，其余为隐藏
 |      :param channels: 卷积通道
 |      :param scale: octave缩放率
 |      :param octaves: octave层数范围
 |      :return:输出图像
 |
 |  read_image(self, iamge_path, max_dim=None)
 |      这是一个用于读取本地图片的函数
 |      :param iamge_path:图片路径
 |      :param max_dim:最大尺寸大小，默认为空即保持原始尺寸
 |      :return:返回一个numpy数组
 |
 |  render_deepdream(self, model, image, steps, step_size, verbose, channels: list = [13], preprosses=True)
 |      绘制deepdream图像，一般模式
 |      :param model: 输入模型
 |      :param image: 输入图像
 |      :param steps: 训练轮次
 |      :param step_size: 训练速率
 |      :param verbose: 训练进度显示模式1为显示，其余为隐藏
 |      :param channels: 卷积通道
 |      :param preprosses: 是否预处理，默认打开
 |      :return: 返回图像
 |
 |  render_deepdream_with_octaves(self, model, image, step_per_octave=100, step_size=0.01, octaves=range(-2, 3), octave_scale=1.3, verbose=1)
 |      绘制deepdream图像，octave分块模式
 |      :param model:输入模型
 |      :param image:输入图像
 |      :param step_per_octave:每层octave训练轮次
 |      :param step_size:训练速率
 |      :param octaves:octave层数范围
 |      :param octave_scale:octave缩放比例
 |      :param verbose:训练进度显示模式1为显示，其余为隐藏
 |      :return:输出图像
 |
 |  save_image(self, image, filename)
 |      :param image: 输入图片
 |      :param filename: 保存文件名
 |      :return: none
 |
 |  set_file_name(self, input)
 |      生成一个标准文件名形如 deep_dream_mixed5.jpg
 |      :param input:输入选取的卷积层名称
 |      :return:文件名
 |
 |  show_image(self, image)
 |      显示图片在jupyter notebook中有效
