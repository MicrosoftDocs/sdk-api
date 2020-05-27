---
UID: NS:iscsidsc.__unnamed_struct_13
title: ISCSI_TARGET_PORTAL_GROUPA (iscsidsc.h)
description: ISCSI_TARGET_PORTAL_GROUP.
helpviewer_keywords: ["*PISCSI_TARGET_PORTAL_GROUPA","ISCSI_TARGET_PORTAL_GROUP","ISCSI_TARGET_PORTAL_GROUP structure [iSCSI Discovery Library API]","ISCSI_TARGET_PORTAL_GROUPA","ISCSI_TARGET_PORTAL_GROUPW","PISCSI_TARGET_PORTAL_GROUP","PISCSI_TARGET_PORTAL_GROUP structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_target_portal_group","iscsidsc/ISCSI_TARGET_PORTAL_GROUP","iscsidsc/ISCSI_TARGET_PORTAL_GROUPA","iscsidsc/ISCSI_TARGET_PORTAL_GROUPW","iscsidsc/PISCSI_TARGET_PORTAL_GROUP"]
old-location: iscsidisc\iscsi_target_portal_group.htm
tech.root: iSCSIDisc
ms.assetid: 8b7e874b-5d2b-4948-98f2-1bcd6d4f8ca6
ms.date: 12/05/2018
ms.keywords: '*PISCSI_TARGET_PORTAL_GROUPA, ISCSI_TARGET_PORTAL_GROUP, ISCSI_TARGET_PORTAL_GROUP structure [iSCSI Discovery Library API], ISCSI_TARGET_PORTAL_GROUPA, ISCSI_TARGET_PORTAL_GROUPW, PISCSI_TARGET_PORTAL_GROUP, PISCSI_TARGET_PORTAL_GROUP structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_portal_group, iscsidsc/ISCSI_TARGET_PORTAL_GROUP, iscsidsc/ISCSI_TARGET_PORTAL_GROUPA, iscsidsc/ISCSI_TARGET_PORTAL_GROUPW, iscsidsc/PISCSI_TARGET_PORTAL_GROUP'
f1_keywords:
- iscsidsc/ISCSI_TARGET_PORTAL_GROUP
dev_langs:
- c++
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_TARGET_PORTAL_GROUPW (Unicode) and ISCSI_TARGET_PORTAL_GROUPA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Iscsidsc.h
api_name:
- ISCSI_TARGET_PORTAL_GROUP
- ISCSI_TARGET_PORTAL_GROUPA
- ISCSI_TARGET_PORTAL_GROUPW
targetos: Windows
req.typenames: ISCSI_TARGET_PORTAL_GROUPA, *PISCSI_TARGET_PORTAL_GROUPA
req.redist: 
ms.custom: 19H1
---

# ISCSI_TARGET_PORTAL_GROUPA structure


## -description


The <b>ISCSI_TARGET_PORTAL_GROUP</b> structure contains information about the portals associated with a portal group.


## -struct-fields




### -field Count

The number of portals in the portal group.


### -field Portals

An array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_target_portala">ISCSI_TARGET_PORTAL</a> structures that describe the portals associated with the portal group. Portal names and addresses are described by either wide-character or ascii strings, depending upon implementation.

