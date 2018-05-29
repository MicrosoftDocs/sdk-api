---
UID: NS:msctf.TF_DISPLAYATTRIBUTE
title: TF_DISPLAYATTRIBUTE
author: windows-sdk-content
description: The TF_DISPLAYATTRIBUTE structure contains display attribute data for rendering text.
old-location: tsf\tf_displayattribute.htm
old-project: TSF
ms.assetid: 29faaa22-ea03-4a2e-a035-7979e2a89fc9
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: TF_DISPLAYATTRIBUTE, TF_DISPLAYATTRIBUTE structure [Text Services Framework], _tsf_tf_displayattribute_ref, msctf/TF_DISPLAYATTRIBUTE, tsf.tf_displayattribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DISPLAYATTRIBUTE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Msctf.h
api_name:
-	TF_DISPLAYATTRIBUTE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

