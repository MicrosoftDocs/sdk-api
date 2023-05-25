---
UID: NS:wmsdkidl.tagWMSCRIPTFORMAT
title: WMSCRIPTFORMAT (wmsdkidl.h)
description: The WMSCRIPTFORMAT structure describes the type of script data used in a script stream.
helpviewer_keywords: ["WMSCRIPTFORMAT","WMSCRIPTFORMAT structure [windows Media Format]","wmformat.wmscriptformat","wmsdkidl/WMSCRIPTFORMAT"]
old-location: wmformat\wmscriptformat.htm
tech.root: wmformat
ms.assetid: b7c513ac-9c28-4556-a0c8-f3e0d6efc735
ms.date: 4/26/2023
ms.keywords: WMSCRIPTFORMAT, WMSCRIPTFORMAT structure [windows Media Format], wmformat.wmscriptformat, wmsdkidl/WMSCRIPTFORMAT
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMSCRIPTFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMSCRIPTFORMAT
 - wmsdkidl/tagWMSCRIPTFORMAT
 - WMSCRIPTFORMAT
 - wmsdkidl/WMSCRIPTFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMSCRIPTFORMAT
---

# WMSCRIPTFORMAT structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMSCRIPTFORMAT</b> structure describes the type of script data used in a script stream.

## -struct-fields

### -field scriptType

GUID identifying the type of script commands in a script stream. Always set to WMSCRIPTTYPE_TwoStrings.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>