---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0003
title: WDSTRANSPORT_NAMESPACE_TYPE (wdstptmgmt.h)
author: windows-sdk-content
description: Determines the type of multicast sessions used for transmitting objects covered by this namespace.
old-location: wds\wdstransport_namespace_type.htm
tech.root: wds
ms.assetid: baba27d2-6df1-4261-b98d-9728ecbb56f2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PWDSTRANSPORT_NAMESPACE_TYPE, WDSTRANSPORT_NAMESPACE_TYPE, WDSTRANSPORT_NAMESPACE_TYPE enumeration [Windows Deployment Services], WdsTptNamespaceTypeAutoCast, WdsTptNamespaceTypeScheduledCastAutoStart, WdsTptNamespaceTypeScheduledCastManualStart, WdsTptNamespaceTypeUnknown, wds.wdstransport_namespace_type, wdstptmgmt/WDSTRANSPORT_NAMESPACE_TYPE, wdstptmgmt/WdsTptNamespaceTypeAutoCast, wdstptmgmt/WdsTptNamespaceTypeScheduledCastAutoStart, wdstptmgmt/WdsTptNamespaceTypeScheduledCastManualStart, wdstptmgmt/WdsTptNamespaceTypeUnknown"
ms.topic: enum
f1_keywords: 
 - "wdstptmgmt/WDSTRANSPORT_NAMESPACE_TYPE"
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_NAMESPACE_TYPE
product: Windows
targetos: Windows
req.typenames: WDSTRANSPORT_NAMESPACE_TYPE, *PWDSTRANSPORT_NAMESPACE_TYPE
req.redist: 
ms.custom: 19H1
---

# WDSTRANSPORT_NAMESPACE_TYPE enumeration


## -description


Determines the type of multicast sessions used for transmitting objects covered by this namespace.


## -enum-fields




### -field WdsTptNamespaceTypeUnknown

Default value that indicates that the namespace type is not yet known. This could also be the case if a new namespace type was introduced in later server versions and this version of WdsTptMgmt has not been updated to fully recognize and classify it.


### -field WdsTptNamespaceTypeAutoCast

Indicates that multicast sessions are to be created automatically by the server based on incoming requests from clients. The server independently decides when to start or end these sessions to optimize performance and reduce network congestion.


### -field WdsTptNamespaceTypeScheduledCastManualStart

Indicates that multicast sessions for this namespace are to be scheduled such that they start only when the administrator manually launches them.


### -field WdsTptNamespaceTypeScheduledCastAutoStart

Indicates that multicast sessions for this namespace are to be automatically started by the system based on criteria the administrator sets, such as a scheduled start time or minimum number of clients.

