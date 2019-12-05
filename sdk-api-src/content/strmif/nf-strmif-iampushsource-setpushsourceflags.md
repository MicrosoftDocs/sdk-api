---
UID: NF:strmif.IAMPushSource.SetPushSourceFlags
title: IAMPushSource::SetPushSourceFlags (strmif.h)
description: The SetPushSourceFlags method sets flags that specify the behavior of the filter. Currently, applications should not call this method, because request flags are not supported and an application should not override the flags set by the filter.
old-location: dshow\iampushsource_setpushsourceflags.htm
tech.root: DirectShow
ms.assetid: c07bbf7e-8d81-4eba-a5a1-fde02e8e8c35
ms.date: 12/05/2018
ms.keywords: IAMPushSource interface [DirectShow],SetPushSourceFlags method, IAMPushSource.SetPushSourceFlags, IAMPushSource::SetPushSourceFlags, IAMPushSourceSetPushSourceFlags, SetPushSourceFlags, SetPushSourceFlags method [DirectShow], SetPushSourceFlags method [DirectShow],IAMPushSource interface, dshow.iampushsource_setpushsourceflags, strmif/IAMPushSource::SetPushSourceFlags
ms.topic: method
f1_keywords:
- strmif/IAMPushSource.SetPushSourceFlags
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
- IAMPushSource.SetPushSourceFlags
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMPushSource::SetPushSourceFlags


## -description



The <code>SetPushSourceFlags</code> method sets flags that specify the behavior of the filter. Currently, applications should not call this method, because request flags are not supported and an application should not override the flags set by the filter.




## -parameters




### -param Flags [in]

Combination of flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-_am_pushsource_flags">AM_PUSHSOURCE_FLAGS</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>
 

 

