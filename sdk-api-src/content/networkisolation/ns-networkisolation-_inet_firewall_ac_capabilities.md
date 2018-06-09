---
UID: NS:networkisolation._INET_FIREWALL_AC_CAPABILITIES
title: "_INET_FIREWALL_AC_CAPABILITIES"
author: windows-sdk-content
description: Contains information about the capabilities of an app container.
old-location: ics\inet_firewall_ac_capabilities.htm
old-project: ICS
ms.assetid: 37386225-0c64-49c0-a21c-cecd8bdb1f1f
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*PINET_FIREWALL_AC_CAPABILITIES, INET_FIREWALL_AC_CAPABILITIES, INET_FIREWALL_AC_CAPABILITIES structure [ICS/ICF], PINET_FIREWALL_AC_CAPABILITIES, PINET_FIREWALL_AC_CAPABILITIES structure pointer [ICS/ICF], _INET_FIREWALL_AC_CAPABILITIES, ics.inet_firewall_ac_capabilities, networkisolation/INET_FIREWALL_AC_CAPABILITIES, networkisolation/PINET_FIREWALL_AC_CAPABILITIES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: networkisolation.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: INET_FIREWALL_AC_CAPABILITIES, *PINET_FIREWALL_AC_CAPABILITIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - INET_FIREWALL_AC_CAPABILITIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _INET_FIREWALL_AC_CAPABILITIES structure


## -description


The <b>INET_FIREWALL_AC_CAPABILITIES</b> structure contains information about the capabilities of an app container.


## -struct-fields




### -field count

Type: <b>DWORD</b>

The number of security identifiers (SIDs) in the <b>capabilities</b> member.


### -field capabilities

Type: <b>SID_AND_ATTRIBUTES*</b>

Security information related to the app container's capabilities.

