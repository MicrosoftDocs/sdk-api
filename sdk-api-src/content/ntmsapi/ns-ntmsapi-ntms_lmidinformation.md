---
UID: NS:ntmsapi._NTMS_LMIDINFORMATION
title: NTMS_LMIDINFORMATION (ntmsapi.h)
description: The NTMS_LMIDINFORMATION structure defines the properties specific to a logical media object.
helpviewer_keywords: ["NTMS_LMIDINFORMATION","NTMS_LMIDINFORMATION structure [Files]","_zaw_ntms_lmidinformation","base.ntms_lmidinformation","fs.ntms_lmidinformation","ntmsapi/NTMS_LMIDINFORMATION"]
old-location: fs\ntms_lmidinformation.htm
tech.root: fs
ms.assetid: f1a003af-101a-4f1f-b644-392e5542e8dd
ms.date: 12/05/2018
ms.keywords: NTMS_LMIDINFORMATION, NTMS_LMIDINFORMATION structure [Files], _zaw_ntms_lmidinformation, base.ntms_lmidinformation, fs.ntms_lmidinformation, ntmsapi/NTMS_LMIDINFORMATION
req.header: ntmsapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NTMS_LMIDINFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NTMS_LMIDINFORMATION
 - ntmsapi/_NTMS_LMIDINFORMATION
 - NTMS_LMIDINFORMATION
 - ntmsapi/NTMS_LMIDINFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntmsapi.h
api_name:
 - NTMS_LMIDINFORMATION
---

# NTMS_LMIDINFORMATION structure


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_LMIDINFORMATION</b> structure defines the properties specific to a logical media object.

## -struct-fields

### -field MediaPool

Unique identifier of the media pool that contains the logical media.

### -field dwNumberOfPartitions

Number of sides in the media object.

## -remarks

The 
<b>NTMS_LMIDINFORMATION</b> structure is included in the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.

## -see-also

<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>