---
UID: NF:strmif.IAMTimecodeDisplay.GetTCDisplayEnable
title: IAMTimecodeDisplay::GetTCDisplayEnable (strmif.h)
description: The GetTCDisplayEnable method determines whether an external device's timecode character generator output is enabled or disabled.
helpviewer_keywords: ["GetTCDisplayEnable","GetTCDisplayEnable method [DirectShow]","GetTCDisplayEnable method [DirectShow]","IAMTimecodeDisplay interface","IAMTimecodeDisplay interface [DirectShow]","GetTCDisplayEnable method","IAMTimecodeDisplay.GetTCDisplayEnable","IAMTimecodeDisplay::GetTCDisplayEnable","IAMTimecodeDisplayGetTCDisplayEnable","dshow.iamtimecodedisplay_gettcdisplayenable","strmif/IAMTimecodeDisplay::GetTCDisplayEnable"]
old-location: dshow\iamtimecodedisplay_gettcdisplayenable.htm
tech.root: dshow
ms.assetid: fe8bac4d-a271-47b3-9737-f115429b50aa
ms.date: 12/05/2018
ms.keywords: GetTCDisplayEnable, GetTCDisplayEnable method [DirectShow], GetTCDisplayEnable method [DirectShow],IAMTimecodeDisplay interface, IAMTimecodeDisplay interface [DirectShow],GetTCDisplayEnable method, IAMTimecodeDisplay.GetTCDisplayEnable, IAMTimecodeDisplay::GetTCDisplayEnable, IAMTimecodeDisplayGetTCDisplayEnable, dshow.iamtimecodedisplay_gettcdisplayenable, strmif/IAMTimecodeDisplay::GetTCDisplayEnable
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTimecodeDisplay::GetTCDisplayEnable
 - strmif/IAMTimecodeDisplay::GetTCDisplayEnable
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
 - IAMTimecodeDisplay.GetTCDisplayEnable
---

# IAMTimecodeDisplay::GetTCDisplayEnable


## -description

The <code>GetTCDisplayEnable</code> method determines whether an external device's timecode character generator output is enabled or disabled.

## -parameters

### -param pState [out]

Pointer to a value indicating whether timecode character generator output is enabled. OATRUE indicates enabled; OAFALSE indicates disabled.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This method is not intended for character rendering inside a filter graph, it is purely intended for hardware displays. Ensure that your external timecode reader or generator has display capability before trying to use this method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtimecodedisplay">IAMTimecodeDisplay Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamtimecodedisplay-settcdisplayenable">IAMTimecodeDisplay::SetTCDisplayEnable</a>