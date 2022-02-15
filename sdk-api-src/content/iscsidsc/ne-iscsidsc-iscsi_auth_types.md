---
UID: NE:iscsidsc.__unnamed_enum_1
title: ISCSI_AUTH_TYPES (iscsidsc.h)
description: ISCSI_AUTH_TYPES enumeration indicates the type of authentication method utilized.
helpviewer_keywords: ["*PISCSI_AUTH_TYPES","ISCSI_AUTH_TYPES","ISCSI_AUTH_TYPES enumeration [iSCSI Discovery Library API]","ISCSI_CHAP_AUTH_TYPE","ISCSI_MUTUAL_CHAP_AUTH_TYPE","ISCSI_NO_AUTH_TYPE","iscsidisc.iscsi_auth_types","iscsidsc/ISCSI_AUTH_TYPES","iscsidsc/ISCSI_CHAP_AUTH_TYPE","iscsidsc/ISCSI_MUTUAL_CHAP_AUTH_TYPE","iscsidsc/ISCSI_NO_AUTH_TYPE"]
old-location: iscsidisc\iscsi_auth_types.htm
tech.root: iSCSIDisc
ms.assetid: 432f1968-e2ca-4594-80cc-0f1a852ec81a
ms.date: 12/05/2018
ms.keywords: '*PISCSI_AUTH_TYPES, ISCSI_AUTH_TYPES, ISCSI_AUTH_TYPES enumeration [iSCSI Discovery Library API], ISCSI_CHAP_AUTH_TYPE, ISCSI_MUTUAL_CHAP_AUTH_TYPE, ISCSI_NO_AUTH_TYPE, iscsidisc.iscsi_auth_types, iscsidsc/ISCSI_AUTH_TYPES, iscsidsc/ISCSI_CHAP_AUTH_TYPE, iscsidsc/ISCSI_MUTUAL_CHAP_AUTH_TYPE, iscsidsc/ISCSI_NO_AUTH_TYPE'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: ISCSI_AUTH_TYPES, *PISCSI_AUTH_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_AUTH_TYPES
 - iscsidsc/PISCSI_AUTH_TYPES
 - ISCSI_AUTH_TYPES
 - iscsidsc/ISCSI_AUTH_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - ISCSI_AUTH_TYPES
---

# ISCSI_AUTH_TYPES enumeration


## -description

The <b>ISCSI_AUTH_TYPES</b> enumeration indicates the type of authentication method utilized.

## -enum-fields

### -field ISCSI_NO_AUTH_TYPE:0

No authentication type was specified.

### -field ISCSI_CHAP_AUTH_TYPE:1

Challenge Handshake Authentication Protocol (CHAP) authentication.

### -field ISCSI_MUTUAL_CHAP_AUTH_TYPE:2

Mutual (2-way) CHAP authentication.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_login_options">ISCSI_LOGIN_OPTIONS</a>
