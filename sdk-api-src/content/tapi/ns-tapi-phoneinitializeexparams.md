---
UID: NS:tapi.phoneinitializeexparams_tag
title: PHONEINITIALIZEEXPARAMS (tapi.h)
description: The PHONEINITIALIZEEXPARAMS structure contains parameters used to establish the association between an application and TAPI; for example, the application's selected event notification mechanism. The phoneInitializeEx function uses this structure.
helpviewer_keywords: ["*LPPHONEINITIALIZEEXPARAMS","LPPHONEINITIALIZEEXPARAMS","LPPHONEINITIALIZEEXPARAMS structure pointer [TAPI 2.2]","PHONEINITIALIZEEXPARAMS","PHONEINITIALIZEEXPARAMS structure [TAPI 2.2]","_tapi2_phoneinitializeexparams_str","tapi/LPPHONEINITIALIZEEXPARAMS","tapi/PHONEINITIALIZEEXPARAMS","tapi2.phoneinitializeexparams_str"]
old-location: tapi2\phoneinitializeexparams_str.htm
tech.root: tapi3
ms.assetid: 465653e4-b88a-42a0-99b0-ce26eeaf99fd
ms.date: 12/05/2018
ms.keywords: '*LPPHONEINITIALIZEEXPARAMS, LPPHONEINITIALIZEEXPARAMS, LPPHONEINITIALIZEEXPARAMS structure pointer [TAPI 2.2], PHONEINITIALIZEEXPARAMS, PHONEINITIALIZEEXPARAMS structure [TAPI 2.2], _tapi2_phoneinitializeexparams_str, tapi/LPPHONEINITIALIZEEXPARAMS, tapi/PHONEINITIALIZEEXPARAMS, tapi2.phoneinitializeexparams_str'
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
req.typenames: PHONEINITIALIZEEXPARAMS, *LPPHONEINITIALIZEEXPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phoneinitializeexparams_tag
 - tapi/phoneinitializeexparams_tag
 - LPPHONEINITIALIZEEXPARAMS
 - tapi/LPPHONEINITIALIZEEXPARAMS
 - PHONEINITIALIZEEXPARAMS
 - tapi/PHONEINITIALIZEEXPARAMS
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
 - PHONEINITIALIZEEXPARAMS
---

# PHONEINITIALIZEEXPARAMS structure


## -description

The 
<b>PHONEINITIALIZEEXPARAMS</b> structure contains parameters used to establish the association between an application and TAPI; for example, the application's selected event notification mechanism. The 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a> function uses this structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwOptions

One of the 
<a href="/windows/desktop/Tapi/phoneinitializeexoption--constants">PHONEINITIALIZEEXOPTION_ Constants</a>. Specifies the event notification mechanism the application desires to use.

### -field Handles

### -field Handles.hEvent

If <b>dwOptions</b> specifies PHONEINITIALIZEEXOPTION_USEEVENT, TAPI returns the event handle in this member.

### -field Handles.hCompletionPort

If <b>dwOptions</b> specifies PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this member the handle of an existing completion port opened using 
<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>.

### -field dwCompletionKey

If <b>dwOptions</b> specifies PHONEINITIALIZEEXOPTION_USECOMPLETIONPORT, the application must specify in this field a value that is returned through the <i>lpCompletionKey</i> parameter of 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> to identify the completion message as a telephony message.

## -remarks

See 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a> for further information on these options.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitializeexa">phoneInitializeEx</a>