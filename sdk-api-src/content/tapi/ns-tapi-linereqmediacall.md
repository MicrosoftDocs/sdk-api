---
UID: NS:tapi.linereqmediacall_tag
title: LINEREQMEDIACALL (tapi.h)
description: Describes a request initiated by a call to the lineGetRequest function. This data structure is obsolete and should not be used.
helpviewer_keywords: ["*LPLINEREQMEDIACALL","LINEREQMEDIACALL","LINEREQMEDIACALL structure [TAPI 2.2]","LPLINEREQMEDIACALL","LPLINEREQMEDIACALL structure pointer [TAPI 2.2]","_tapi2_linereqmediacall_str","tapi/LINEREQMEDIACALL","tapi/LPLINEREQMEDIACALL","tapi2.linereqmediacall_str"]
old-location: tapi2\linereqmediacall_str.htm
tech.root: tapi3
ms.assetid: 4b0e4919-ebf9-496c-a8c9-bb8357879c65
ms.date: 12/05/2018
ms.keywords: '*LPLINEREQMEDIACALL, LINEREQMEDIACALL, LINEREQMEDIACALL structure [TAPI 2.2], LPLINEREQMEDIACALL, LPLINEREQMEDIACALL structure pointer [TAPI 2.2], _tapi2_linereqmediacall_str, tapi/LINEREQMEDIACALL, tapi/LPLINEREQMEDIACALL, tapi2.linereqmediacall_str'
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
req.typenames: LINEREQMEDIACALL, *LPLINEREQMEDIACALL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linereqmediacall_tag
 - tapi/linereqmediacall_tag
 - LPLINEREQMEDIACALL
 - tapi/LPLINEREQMEDIACALL
 - LINEREQMEDIACALL
 - tapi/LINEREQMEDIACALL
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
 - LINEREQMEDIACALL
---

# LINEREQMEDIACALL structure


## -description

The 
<b>LINEREQMEDIACALL</b> structure describes a request initiated by a call to the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a> function. This data structure is obsolete and should not be used.

## -struct-fields

### -field hWnd

A handle to the window of the application that  made the request.

### -field wRequestID

The identifier of the request. Used to match an asynchronous response.

### -field szDeviceClass

The device class required to fill the request.

### -field ucDeviceID

The device identifier.

### -field dwSize

Size, in bytes, of this structure.

### -field dwSecure

Not used.

### -field szDestAddress

The destination address.

### -field szAppName

The name of application that made the request.

### -field szCalledParty

The called party name.

### -field szComment

The comment buffer.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-linegetrequest">lineGetRequest</a>