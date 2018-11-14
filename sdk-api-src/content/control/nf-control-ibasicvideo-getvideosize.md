---
UID: NF:control.IBasicVideo.GetVideoSize
title: IBasicVideo::GetVideoSize
author: windows-sdk-content
description: The GetVideoSize method retrieves the native video dimensions.
old-location: dshow\ibasicvideo_getvideosize.htm
tech.root: DirectShow
ms.assetid: fbabba8b-b86b-451b-ad06-4454174ee352
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetVideoSize, GetVideoSize method [DirectShow], GetVideoSize method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetVideoSize method, IBasicVideo.GetVideoSize, IBasicVideo::GetVideoSize, IBasicVideoGetVideoSize, control/IBasicVideo::GetVideoSize, dshow.ibasicvideo_getvideosize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBasicVideo.GetVideoSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- control.h
: 
- IBasicVideo.GetVideoSize
: 
---

# IBasicVideo::GetVideoSize


## -description



The <code>GetVideoSize</code> method retrieves the native video dimensions.




## -parameters




### -param pWidth [out]

Pointer to a variable that receives the width of the video image, in pixels.


### -param pHeight [out]

Pointer to a variable that receives the height of the video image, in pixels.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

