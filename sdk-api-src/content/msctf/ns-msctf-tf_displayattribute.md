---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TF_DISPLAYATTRIBUTE structure


## -description



The <b>TF_DISPLAYATTRIBUTE</b> structure contains display attribute data for rendering text.




## -struct-fields




### -field crText

Contains a <a href="https://msdn.microsoft.com/0ce8f941-c187-437f-8bad-f882e63b8421">TF_DA_COLOR</a> structure that defines the text foreground color.


### -field crBk

Contains a <b>TF_DA_COLOR</b> structure that defines the text background color.


### -field lsStyle

Contains a <a href="https://msdn.microsoft.com/36ea6359-e25a-4b23-8d9d-961d743268ab">TF_DA_LINESTYLE</a> enumeration value that defines the underline style.


### -field fBoldLine

A BOOL value that specifies if the underline should be bold or normal weight. If this value is nonzero, the underline should be bold. If this value is zero, the underline should be normal.


### -field crLine

Contains a <b>TF_DA_COLOR</b> structure that defines the color of the underline.


### -field bAttr

Contains a <a href="https://msdn.microsoft.com/894e6c15-d911-4e0c-96b1-db6ec8e43eba">TF_DA_ATTR_INFO</a> value that defines text conversion display attribute data.


## -see-also




<a href="https://msdn.microsoft.com/894e6c15-d911-4e0c-96b1-db6ec8e43eba">TF_DA_ATTR_INFO
      </a>



<a href="https://msdn.microsoft.com/0ce8f941-c187-437f-8bad-f882e63b8421">
        TF_DA_COLOR
      </a>



<a href="https://msdn.microsoft.com/36ea6359-e25a-4b23-8d9d-961d743268ab">
        TF_DA_LINESTYLE
      </a>
 

 

