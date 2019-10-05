---
UID: NF:strmif.IAMPushSource.GetPushSourceFlags
title: IAMPushSource::GetPushSourceFlags (strmif.h)
author: windows-sdk-content
description: The GetPushSourceFlags method retrieves a combination of flags describing the behavior of the filter.
old-location: dshow\iampushsource_getpushsourceflags.htm
tech.root: DirectShow
ms.assetid: 3e72367f-a066-43ad-9f96-648cad13b43d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPushSourceFlags, GetPushSourceFlags method [DirectShow], GetPushSourceFlags method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetPushSourceFlags method, IAMPushSource.GetPushSourceFlags, IAMPushSource::GetPushSourceFlags, IAMPushSourceGetPushSourceFlags, dshow.iampushsource_getpushsourceflags, strmif/IAMPushSource::GetPushSourceFlags
ms.topic: method
f1_keywords: 
 - "strmif/IAMPushSource.GetPushSourceFlags"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMPushSource::GetPushSourceFlags


## -description



The <code>GetPushSourceFlags</code> method retrieves a combination of flags describing the behavior of the filter.




## -parameters




### -param pFlags [out]

Pointer to a variable that receives a combination of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_am_pushsource_flags">AM_PUSHSOURCE_FLAGS</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



Call this method to determine whether a renderer filter can safely match clock rates with this source filter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>
 

 

