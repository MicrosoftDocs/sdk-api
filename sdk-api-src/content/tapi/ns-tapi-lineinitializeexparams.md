---
UID: NS:tapi.lineinitializeexparams_tag
title: LINEINITIALIZEEXPARAMS (tapi.h)
description: The LINEINITIZALIZEEXPARAMS structure describes parameters supplied when making calls using LINEINITIALIZEEX.
helpviewer_keywords: ["*LPLINEINITIALIZEEXPARAMS","LINEINITIALIZEEXPARAMS","LINEINITIALIZEEXPARAMS structure [TAPI 2.2]","LPLINEINITIALIZEEXPARAMS","LPLINEINITIALIZEEXPARAMS structure pointer [TAPI 2.2]","_tapi2_lineinitializeexparams_str","tapi/LINEINITIALIZEEXPARAMS","tapi/LPLINEINITIALIZEEXPARAMS","tapi2.lineinitializeexparams_str"]
old-location: tapi2\lineinitializeexparams_str.htm
tech.root: tapi3
ms.assetid: 17fed282-6d08-4702-9ceb-9cbcc3737395
ms.date: 12/05/2018
ms.keywords: '*LPLINEINITIALIZEEXPARAMS, LINEINITIALIZEEXPARAMS, LINEINITIALIZEEXPARAMS structure [TAPI 2.2], LPLINEINITIALIZEEXPARAMS, LPLINEINITIALIZEEXPARAMS structure pointer [TAPI 2.2], _tapi2_lineinitializeexparams_str, tapi/LINEINITIALIZEEXPARAMS, tapi/LPLINEINITIALIZEEXPARAMS, tapi2.lineinitializeexparams_str'
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: LINEINITIALIZEEXPARAMS, *LPLINEINITIALIZEEXPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineinitializeexparams_tag
 - tapi/lineinitializeexparams_tag
 - LPLINEINITIALIZEEXPARAMS
 - tapi/LPLINEINITIALIZEEXPARAMS
 - LINEINITIALIZEEXPARAMS
 - tapi/LINEINITIALIZEEXPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEINITIALIZEEXPARAMS
---

# LINEINITIALIZEEXPARAMS structure


## -description

The <b>LINEINITIZALIZEEXPARAMS</b> structure describes parameters supplied when making calls using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">LINEINITIALIZEEX</a>.

## -struct-fields

### -field dwTotalSize

Total size, in bytes, allocated to this data structure.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwOptions

One of the 
<a href="/windows/desktop/Tapi/lineinitializeexoption--constants">LINEINITIALIZEEXOPTION_ Constants</a>. Specifies the event notification mechanism the application desires to use.

### -field Handles

### -field Handles.hEvent

If <b>dwOptions</b> specifies LINEINITIALIZEEXOPTION_USEEVENT, TAPI returns the event handle in this field.

### -field Handles.hCompletionPort

If <b>dwOptions</b> specifies LINEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this field the handle of an existing completion port opened using 
<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>.

### -field dwCompletionKey

If <b>dwOptions</b> specifies LINEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this field a value that is returned through the <i>lpCompletionKey</i> parameter of 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> to identify the completion message as a telephony message.

## -remarks

See 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a> for further information on these options.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-lineinitializeexa">lineInitializeEx</a>