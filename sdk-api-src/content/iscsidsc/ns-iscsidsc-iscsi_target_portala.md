---
UID: NS:iscsidsc.ISCSI_TARGET_PORTALA
title: ISCSI_TARGET_PORTALA
author: windows-sdk-content
description: ISCSI_TARGET_PORTAL structure contains information about a portal.
old-location: iscsidisc\iscsi_target_portal.htm
old-project: iSCSIDisc
ms.assetid: de78c7ec-c2ce-493a-ad29-2ea10e3d7dff
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: "*PISCSI_TARGET_PORTALA, ISCSI_TARGET_PORTAL, ISCSI_TARGET_PORTAL structure [iSCSI Discovery Library API], ISCSI_TARGET_PORTALA, ISCSI_TARGET_PORTALW, PISCSI_TARGET_PORTAL, PISCSI_TARGET_PORTAL structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_portal, iscsidsc/ISCSI_TARGET_PORTAL, iscsidsc/ISCSI_TARGET_PORTALA, iscsidsc/ISCSI_TARGET_PORTALW, iscsidsc/PISCSI_TARGET_PORTAL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_TARGET_PORTALW (Unicode) and ISCSI_TARGET_PORTALA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ISCSI_TARGET_PORTALA, *PISCSI_TARGET_PORTALA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iscsidsc.h
api_name:
 - ISCSI_TARGET_PORTAL
 - ISCSI_TARGET_PORTALA
 - ISCSI_TARGET_PORTALW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISCSI_TARGET_PORTALA structure


## -description


The <b>ISCSI_TARGET_PORTAL</b> structure contains information about a portal.


## -struct-fields




### -field SymbolicName

A string representing the name of the portal.


### -field Address

A string representing the IP address or DNS name of the portal.


### -field Socket

The socket number of the portal.

