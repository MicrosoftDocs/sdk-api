---
UID: NS:netfw._INET_FIREWALL_AC_BINARIES
title: "_INET_FIREWALL_AC_BINARIES"
author: windows-driver-content
description: Contains the binary paths to applications running in an app container.
old-location: ics\inet_firewall_ac_binaries.htm
old-project: ICS
ms.assetid: 5403303e-e65c-47cf-af84-3d748db8661b
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*PINET_FIREWALL_AC_BINARIES, INET_FIREWALL_AC_BINARIES, INET_FIREWALL_AC_BINARIES structure [ICS/ICF], PINET_FIREWALL_AC_BINARIES, PINET_FIREWALL_AC_BINARIES structure pointer [ICS/ICF], _INET_FIREWALL_AC_BINARIES, ics.inet_firewall_ac_binaries, networkisolation/INET_FIREWALL_AC_BINARIES, networkisolation/PINET_FIREWALL_AC_BINARIES"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: netfw.h
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
req.typenames: INET_FIREWALL_AC_BINARIES, *PINET_FIREWALL_AC_BINARIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	networkisolation.h
api_name:
-	INET_FIREWALL_AC_BINARIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _INET_FIREWALL_AC_BINARIES structure


## -description


The <b>INET_FIREWALL_AC_BINARIES</b> structure contains the binary paths to applications running in an app container.


## -struct-fields




### -field count

The number of paths in the <b>binaries</b> member.


### -field binaries

Paths to the applications running in the app container.

