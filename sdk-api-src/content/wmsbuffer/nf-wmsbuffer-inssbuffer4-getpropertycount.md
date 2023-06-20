---
UID: NF:wmsbuffer.INSSBuffer4.GetPropertyCount
title: INSSBuffer4::GetPropertyCount (wmsbuffer.h)
description: The GetPropertyCount method retrieves the total number of buffer properties, also called data unit extensions, associated with the sample contained in the buffer object.
helpviewer_keywords: ["GetPropertyCount","GetPropertyCount method [windows Media Format]","GetPropertyCount method [windows Media Format]","INSSBuffer4 interface","INSSBuffer4 interface [windows Media Format]","GetPropertyCount method","INSSBuffer4.GetPropertyCount","INSSBuffer4::GetPropertyCount","INSSBuffer4GetPropertyCount","wmformat.inssbuffer4_getpropertycount","wmsbuffer/INSSBuffer4::GetPropertyCount"]
old-location: wmformat\inssbuffer4_getpropertycount.htm
tech.root: wmformat
ms.assetid: b47f26b3-e816-498d-adc3-c6d3357971e6
ms.date: 4/26/2023
ms.keywords: GetPropertyCount, GetPropertyCount method [windows Media Format], GetPropertyCount method [windows Media Format],INSSBuffer4 interface, INSSBuffer4 interface [windows Media Format],GetPropertyCount method, INSSBuffer4.GetPropertyCount, INSSBuffer4::GetPropertyCount, INSSBuffer4GetPropertyCount, wmformat.inssbuffer4_getpropertycount, wmsbuffer/INSSBuffer4::GetPropertyCount
req.header: wmsbuffer.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INSSBuffer4::GetPropertyCount
 - wmsbuffer/INSSBuffer4::GetPropertyCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - INSSBuffer4.GetPropertyCount
---

# INSSBuffer4::GetPropertyCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetPropertyCount</b> method retrieves the total number of buffer properties, also called data unit extensions, associated with the sample contained in the buffer object. When using <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer4-getpropertybyindex">INSSBuffer4::GetPropertyByIndex</a> to retrieve properties, the index used is between zero and the number specified by this method.

## -parameters

### -param pcBufferProperties [out]

Pointer to the size of buffer properties.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4">INSSBuffer4 Interface</a>