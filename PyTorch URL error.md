
  import torchvision.models as models
  model = models.ResNet50(pretrained=True)
'''
raise error:
ssl.SSLError: [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:847)
solution：
add codes as:
'''
  import torchvision.models as models
  import ssl
  ssl._create_default_https_context = ssl._create_unverified_context
  model = models.ResNet50(pretrained=True)
