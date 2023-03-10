---
UID: NF:strmif.IAMPushSource.GetPushSourceFlags
title: IAMPushSource::GetPushSourceFlags (strmif.h)
description: The GetPushSourceFlags method retrieves a combination of flags describing the behavior of the filter.
helpviewer_keywords: ["GetPushSourceFlags","GetPushSourceFlags method [DirectShow]","GetPushSourceFlags method [DirectShow]","IAMPushSource interface","IAMPushSource interface [DirectShow]","GetPushSourceFlags method","IAMPushSource.GetPushSourceFlags","IAMPushSource::GetPushSourceFlags","IAMPushSourceGetPushSourceFlags","dshow.iampushsource_getpushsourceflags","strmif/IAMPushSource::GetPushSourceFlags"]
old-location: dshow\iampushsource_getpushsourceflags.htm
tech.root: dshow
ms.assetid: 3e72367f-a066-43ad-9f96-648cad13b43d
ms.date: 12/05/2018
ms.keywords: GetPushSourceFlags, GetPushSourceFlags method [DirectShow], GetPushSourceFlags method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetPushSourceFlags method, IAMPushSource.GetPushSourceFlags, IAMPushSource::GetPushSourceFlags, IAMPushSourceGetPushSourceFlags, dshow.iampushsource_getpushsourceflags, strmif/IAMPushSource::GetPushSourceFlags
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMPushSource::GetPushSourceFlags
 - strmif/IAMPushSource::GetPushSourceFlags
dev_langs:
 - c++
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
---

# IAMPushSource::GetPushSourceFlags


## -description

The <code>GetPushSourceFlags</code> method retrieves a combination of flags describing the behavior of the filter.

## -parameters

### -param pFlags [out]

Pointer to a variable that receives a combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-_am_pushsource_flags">AM_PUSHSOURCE_FLAGS</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

Call this method to determine whether a renderer filter can safely match clock rates with this source filter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>