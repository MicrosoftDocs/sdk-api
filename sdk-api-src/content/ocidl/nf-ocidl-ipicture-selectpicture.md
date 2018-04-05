---
UID: NF:ocidl.IPicture.SelectPicture
title: IPicture::SelectPicture method
author: windows-driver-content
description: Selects a bitmap picture into a given device context, and returns the device context in which the picture was previously selected as well as the picture's GDI handle. This method works in conjunction with IPicture::get_CurDC.
old-location: com\ipicture_selectpicture.htm
old-project: com
ms.assetid: 4168dbf7-ccc3-49ee-9b04-b0370eb389af
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IPicture, IPicture interface [COM], SelectPicture method, IPicture::SelectPicture, SelectPicture method [COM], SelectPicture method [COM], IPicture interface, SelectPicture,IPicture.SelectPicture, _ctrl_ipicture_selectpicture, com.ipicture_selectpicture, ocidl/IPicture::SelectPicture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPicture.SelectPicture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPicture::SelectPicture method


## -description


Selects a bitmap picture into a given device context, and returns the device context in which the picture was previously selected as well as the picture's GDI handle. This method works in conjunction with <a href="https://msdn.microsoft.com/a5c13a54-692d-423f-824d-5a96c137dec9">IPicture::get_CurDC</a>.


## -parameters




### -param hDCIn [in]

A handle for the device context in which to select the picture.


### -param phDCOut [out]

A pointer to a variable that receives the previous device context. This parameter can be <b>NULL</b> if the caller does not need this information. Ownership of the device context is always the responsibility of the caller.


### -param phBmpOut [out]

A pointer to a variable that receives the GDI handle of the picture. This parameter can be <b>NULL</b> if the caller does not need the handle. Ownership of this handle is determined by the <i>fOwn</i> parameter passed to <a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect</a>. Pictures loaded from a stream always own their resources.


## -returns



This method supports the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>



<a href="https://msdn.microsoft.com/a5c13a54-692d-423f-824d-5a96c137dec9">IPicture::get_CurDC</a>
 

 

