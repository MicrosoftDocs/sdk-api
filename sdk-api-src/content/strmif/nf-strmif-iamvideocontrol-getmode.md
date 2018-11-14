---
UID: NF:strmif.IAMVideoControl.GetMode
title: IAMVideoControl::GetMode
author: windows-sdk-content
description: The GetMode method retrieves the video control mode of operation.
old-location: dshow\iamvideocontrol_getmode.htm
tech.root: DirectShow
ms.assetid: 4b937661-67b2-445c-ab25-8655e1036797
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMode, GetMode method [DirectShow], GetMode method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetMode method, IAMVideoControl.GetMode, IAMVideoControl::GetMode, IAMVideoControlGetMode, dshow.iamvideocontrol_getmode, strmif/IAMVideoControl::GetMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
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
 - IAMVideoControl.GetMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMVideoControl.GetMode
: 
---

# IAMVideoControl::GetMode


## -description



The <code>GetMode</code> method retrieves the video control mode of operation.




## -parameters




### -param pPin [in]

Pointer to the pin to retrieve the video control mode from.


### -param Mode [out]

Pointer to a value representing a combination of the flags from the <a href="https://msdn.microsoft.com/9d7feb46-fb07-46d8-a9a5-511578873cf3">VideoControlFlags</a> enumeration, which specify the video control mode.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Possible modes of operation include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd114977-c76c-4429-a835-98601b350a93">IAMVideoControl Interface</a>
 

 

