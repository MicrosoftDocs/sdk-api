---
UID: NE:networkisolation._INET_FIREWALL_AC_CREATION_TYPE
title: "_INET_FIREWALL_AC_CREATION_TYPE"
author: windows-sdk-content
description: Specifies the type of app container creation events for which notifications will be delivered.
old-location: ics\inet_firewall_ac_creation_type.htm
tech.root: ics
ms.assetid: 01a1f735-889e-424e-860e-ca86f0abd126
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INET_FIREWALL_AC_BINARY, INET_FIREWALL_AC_CREATION_TYPE, INET_FIREWALL_AC_CREATION_TYPE enumeration [ICS/ICF], INET_FIREWALL_AC_MAX, INET_FIREWALL_AC_NONE, INET_FIREWALL_AC_PACKAGE_ID_ONLY, _INET_FIREWALL_AC_CREATION_TYPE, ics.inet_firewall_ac_creation_type, networkisolation/INET_FIREWALL_AC_BINARY, networkisolation/INET_FIREWALL_AC_CREATION_TYPE, networkisolation/INET_FIREWALL_AC_MAX, networkisolation/INET_FIREWALL_AC_NONE, networkisolation/INET_FIREWALL_AC_PACKAGE_ID_ONLY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - INET_FIREWALL_AC_CREATION_TYPE
product: Windows
targetos: Windows
req.typenames: INET_FIREWALL_AC_CREATION_TYPE
req.redist: 
---

# _INET_FIREWALL_AC_CREATION_TYPE enumeration


## -description


The <b>INET_FIREWALL_AC_CREATION_TYPE</b> enumeration specifies the type of app container creation events for which notifications will be delivered.


## -enum-fields




### -field INET_FIREWALL_AC_NONE

This value is reserved for system use.


### -field INET_FIREWALL_AC_PACKAGE_ID_ONLY

Notifications will be delivered when an app container is created with a package identifier.


### -field INET_FIREWALL_AC_BINARY

Notifications will be delivered when an app container is created with a binary path.


### -field INET_FIREWALL_AC_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/b5f1b85d-3538-4be3-b97b-f9207cc7063b">INET_FIREWALL_AC_CHANGE</a>
 

 

