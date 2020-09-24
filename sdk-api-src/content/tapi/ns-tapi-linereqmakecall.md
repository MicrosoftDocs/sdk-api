---
UID: NS:tapi.linereqmakecall_tag
title: LINEREQMAKECALL (tapi.h)
description: The LINEREQMAKECALL structure describes a request initiated by a call to the lineGetRequest function.
helpviewer_keywords: ["*LPLINEREQMAKECALL","LINEREQMAKECALL","LINEREQMAKECALL structure [TAPI 2.2]","LPLINEREQMAKECALL","LPLINEREQMAKECALL structure pointer [TAPI 2.2]","_tapi2_linereqmakecall_str","tapi/LINEREQMAKECALL","tapi/LPLINEREQMAKECALL","tapi2.linereqmakecall_str"]
old-location: tapi2\linereqmakecall_str.htm
tech.root: tapi3
ms.assetid: de4e51af-ea1c-41aa-b5a9-9fa628e18d9d
ms.date: 12/05/2018
ms.keywords: '*LPLINEREQMAKECALL, LINEREQMAKECALL, LINEREQMAKECALL structure [TAPI 2.2], LPLINEREQMAKECALL, LPLINEREQMAKECALL structure pointer [TAPI 2.2], _tapi2_linereqmakecall_str, tapi/LINEREQMAKECALL, tapi/LPLINEREQMAKECALL, tapi2.linereqmakecall_str'
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
req.typenames: LINEREQMAKECALL, *LPLINEREQMAKECALL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linereqmakecall_tag
 - tapi/linereqmakecall_tag
 - LPLINEREQMAKECALL
 - tapi/LPLINEREQMAKECALL
 - LINEREQMAKECALL
 - tapi/LINEREQMAKECALL
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
 - LINEREQMAKECALL
---

# LINEREQMAKECALL structure


## -description

The 
<b>LINEREQMAKECALL</b> structure describes a request initiated by a call to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a> function.

## -struct-fields

### -field szDestAddress

<b>Null</b>-terminated destination address of the make-call request. The address can use the canonical address format or the dialable address format. The maximum length of the address is TAPIMAXDESTADDRESSSIZE characters, which includes the <b>NULL</b> terminator. Longer strings are truncated.

### -field szAppName

<b>Null</b>-terminated user-friendly application name or filename of the application that originated the request. The maximum length of the address is TAPIMAXAPPNAMESIZE characters, which includes the <b>NULL</b> terminator.

### -field szCalledParty

<b>Null</b>-terminated user-friendly called-party name. The maximum length of the called-party information is TAPIMAXCALLEDPARTYSIZE characters, which includes the <b>NULL</b> terminator.

### -field szComment

<b>Null</b>-terminated comment about the call request. The maximum length of the comment string is TAPIMAXCOMMENTSIZE characters, which includes the <b>NULL</b> terminator.

## -remarks

This structure may not be extended.

The <b>szDestAddress</b> member contains the address of the remote party; the other members are useful for logging purposes. An application must use this structure to interpret the request buffer it received from 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a> with the LINEREQUESTMODE_MAKECALL request mode.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a>