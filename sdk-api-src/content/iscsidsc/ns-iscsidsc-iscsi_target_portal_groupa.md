---
UID: NS:iscsidsc.ISCSI_TARGET_PORTAL_GROUPA
title: ISCSI_TARGET_PORTAL_GROUPA
author: windows-driver-content
description: ISCSI_TARGET_PORTAL_GROUP.
old-location: iscsidisc\iscsi_target_portal_group.htm
old-project: iSCSIDisc
ms.assetid: 8b7e874b-5d2b-4948-98f2-1bcd6d4f8ca6
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PISCSI_TARGET_PORTAL_GROUPA, ISCSI_TARGET_PORTAL_GROUP, ISCSI_TARGET_PORTAL_GROUP structure [iSCSI Discovery Library API], ISCSI_TARGET_PORTAL_GROUPA, ISCSI_TARGET_PORTAL_GROUPW, PISCSI_TARGET_PORTAL_GROUP, PISCSI_TARGET_PORTAL_GROUP structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_portal_group, iscsidsc/ISCSI_TARGET_PORTAL_GROUP, iscsidsc/ISCSI_TARGET_PORTAL_GROUPA, iscsidsc/ISCSI_TARGET_PORTAL_GROUPW, iscsidsc/PISCSI_TARGET_PORTAL_GROUP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.namespace: Root\WMI
req.assembly: 
req.type-library: 
req.typenames: ISCSI_TARGET_PORTAL_GROUPA, *PISCSI_TARGET_PORTAL_GROUPA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iscsidsc.h
api_name:
-	ISCSI_TARGET_PORTAL_GROUP
-	ISCSI_TARGET_PORTAL_GROUPA
-	ISCSI_TARGET_PORTAL_GROUPW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISCSI_TARGET_PORTAL_GROUPA structure


## -description


The <b>ISCSI_TARGET_PORTAL_GROUP</b> structure contains information about the portals associated with a portal group.


## -struct-fields




### -field Count

The number of portals in the portal group.


### -field Portals

An array of <a href="https://msdn.microsoft.com/de78c7ec-c2ce-493a-ad29-2ea10e3d7dff">ISCSI_TARGET_PORTAL</a> structures that describe the portals associated with the portal group. Portal names and addresses are described by either wide-character or ascii strings, depending upon implementation.

