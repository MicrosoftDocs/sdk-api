---
UID: NS:winnt._SID_AND_ATTRIBUTES
title: SID_AND_ATTRIBUTES (winnt.h)
description: Represents a security identifier (SID) and its attributes.
helpviewer_keywords: ["*PSID_AND_ATTRIBUTES","PSID_AND_ATTRIBUTES","PSID_AND_ATTRIBUTES structure pointer [Security]","SID_AND_ATTRIBUTES","SID_AND_ATTRIBUTES structure [Security]","_SID_AND_ATTRIBUTES","_win32_sid_and_attributes_str","security.sid_and_attributes","winnt/PSID_AND_ATTRIBUTES","winnt/SID_AND_ATTRIBUTES"]
old-location: security\sid_and_attributes.htm
tech.root: security
ms.assetid: d15d5a3f-6b38-4b92-b59c-ff0d27d111d9
ms.date: 12/05/2018
ms.keywords: '*PSID_AND_ATTRIBUTES, PSID_AND_ATTRIBUTES, PSID_AND_ATTRIBUTES structure pointer [Security], SID_AND_ATTRIBUTES, SID_AND_ATTRIBUTES structure [Security], _SID_AND_ATTRIBUTES, _win32_sid_and_attributes_str, security.sid_and_attributes, winnt/PSID_AND_ATTRIBUTES, winnt/SID_AND_ATTRIBUTES'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: SID_AND_ATTRIBUTES, *PSID_AND_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID_AND_ATTRIBUTES
 - winnt/_SID_AND_ATTRIBUTES
 - PSID_AND_ATTRIBUTES
 - winnt/PSID_AND_ATTRIBUTES
 - SID_AND_ATTRIBUTES
 - winnt/SID_AND_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SID_AND_ATTRIBUTES
---

# SID_AND_ATTRIBUTES structure


## -description

The <b>SID_AND_ATTRIBUTES</b> structure represents a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) and its attributes. SIDs are used to uniquely identify users or groups.

## -struct-fields

### -field Sid

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

### -field Attributes

Specifies attributes of the SID. This value contains up to 32 one-bit flags. Its meaning depends on the definition and use of the SID.

## -remarks

A group is represented by a SID. SIDs have attributes that indicate whether they are currently enabled, disabled, or mandatory. SIDs also indicate how these attributes are used. A <b>SID_AND_ATTRIBUTES</b> structure can represent a SID whose attributes change frequently. For example, <b>SID_AND_ATTRIBUTES</b> is used to represent groups in the <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_user">TOKEN_USER</a>