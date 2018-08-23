---
UID: NF:strmif.IAMVideoControl.GetCaps
title: IAMVideoControl::GetCaps
author: windows-sdk-content
description: The GetCaps method retrieves the capabilities of the underlying hardware.
old-location: dshow\iamvideocontrol_getcaps.htm
old-project: DirectShow
ms.assetid: 8e4b7b46-8179-410c-8369-652f9b65de8c
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetCaps, GetCaps method [DirectShow], GetCaps method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetCaps method, IAMVideoControl.GetCaps, IAMVideoControl::GetCaps, IAMVideoControlGetCaps, dshow.iamvideocontrol_getcaps, strmif/IAMVideoControl::GetCaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMVideoControl.GetCaps
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoControl::GetCaps


## -description



The <code>GetCaps</code> method retrieves the capabilities of the underlying hardware.




## -parameters




### -param pPin [in]

Pointer to the pin to query capabilities from.


### -param pCapsFlags [out]

Pointer to a value representing a combination of the flags from the <a href="https://msdn.microsoft.com/9d7feb46-fb07-46d8-a9a5-511578873cf3">VideoControlFlags</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Possible capabilities include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd114977-c76c-4429-a835-98601b350a93">IAMVideoControl Interface</a>
 

 

