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

# IPicture::SelectPicture


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
 

 

