---
UID: NF:strmif.IAMPushSource.GetPushSourceFlags
title: IAMPushSource::GetPushSourceFlags
author: windows-sdk-content
description: The GetPushSourceFlags method retrieves a combination of flags describing the behavior of the filter.
old-location: dshow\iampushsource_getpushsourceflags.htm
tech.root: DirectShow
ms.assetid: 3e72367f-a066-43ad-9f96-648cad13b43d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPushSourceFlags, GetPushSourceFlags method [DirectShow], GetPushSourceFlags method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetPushSourceFlags method, IAMPushSource.GetPushSourceFlags, IAMPushSource::GetPushSourceFlags, IAMPushSourceGetPushSourceFlags, dshow.iampushsource_getpushsourceflags, strmif/IAMPushSource::GetPushSourceFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMPushSource.GetPushSourceFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMPushSource::GetPushSourceFlags


## -description



The <code>GetPushSourceFlags</code> method retrieves a combination of flags describing the behavior of the filter.




## -parameters




### -param pFlags [out]

Pointer to a variable that receives a combination of flags from the <a href="https://msdn.microsoft.com/878dc41b-8df3-4294-9e1f-7a3da1834ad1">AM_PUSHSOURCE_FLAGS</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Call this method to determine whether a renderer filter can safely match clock rates with this source filter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5ab294a8-f250-405c-a589-68998bc04cdf">IAMPushSource Interface</a>
 

 

