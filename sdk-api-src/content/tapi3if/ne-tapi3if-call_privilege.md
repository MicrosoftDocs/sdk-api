---
UID: NE:tapi3if.CALL_PRIVILEGE
title: CALL_PRIVILEGE (tapi3if.h)
description: A CALL_PRIVILEGE member is returned by the ITCallInfo::get_Privilege method, and indicates when the current application owns or is monitoring the current call.
helpviewer_keywords: ["CALL_PRIVILEGE","CALL_PRIVILEGE enumeration [TAPI 2.2]","CP_MONITOR","CP_OWNER","_tapi3_call_privilege","tapi3.call_privilege","tapi3if/CALL_PRIVILEGE","tapi3if/CP_MONITOR","tapi3if/CP_OWNER"]
old-location: tapi3\call_privilege.htm
tech.root: tapi3
ms.assetid: 8d2ab3d2-9531-40fc-910d-2bd81a075cc3
ms.date: 12/05/2018
ms.keywords: CALL_PRIVILEGE, CALL_PRIVILEGE enumeration [TAPI 2.2], CP_MONITOR, CP_OWNER, _tapi3_call_privilege, tapi3.call_privilege, tapi3if/CALL_PRIVILEGE, tapi3if/CP_MONITOR, tapi3if/CP_OWNER
req.header: tapi3if.h
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
req.typenames: CALL_PRIVILEGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CALL_PRIVILEGE
 - tapi3if/CALL_PRIVILEGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - CALL_PRIVILEGE
---

# CALL_PRIVILEGE enumeration


## -description

A 
<b>CALL_PRIVILEGE</b> member is returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege">ITCallInfo::get_Privilege</a> method, and indicates when the current application owns or is monitoring the current call.

## -enum-fields

### -field CP_OWNER:0

The application is the owner of the call.

### -field CP_MONITOR

The application is a monitor of the call.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege">ITCallInfo::get_Privilege</a>
