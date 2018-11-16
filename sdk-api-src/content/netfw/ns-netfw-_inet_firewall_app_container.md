---
UID: NS:netfw._INET_FIREWALL_APP_CONTAINER
title: "_INET_FIREWALL_APP_CONTAINER"
author: windows-sdk-content
description: Contains information about an specific app container.
old-location: ics\inet_firewall_app_container.htm
tech.root: ICS
ms.assetid: 0567fb66-0511-4c80-9e31-2412507ced97
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PINET_FIREWALL_APP_CONTAINER, INET_FIREWALL_APP_CONTAINER, INET_FIREWALL_APP_CONTAINER structure [ICS/ICF], PINET_FIREWALL_APP_CONTAINER, PINET_FIREWALL_APP_CONTAINER structure pointer [ICS/ICF], _INET_FIREWALL_APP_CONTAINER, ics.inet_firewall_app_container, networkisolation/INET_FIREWALL_APP_CONTAINER, networkisolation/PINET_FIREWALL_APP_CONTAINER"
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
 - INET_FIREWALL_APP_CONTAINER
product: Windows
targetos: Windows
req.typenames: INET_FIREWALL_APP_CONTAINER, *PINET_FIREWALL_APP_CONTAINER
req.redist: 
---

# _INET_FIREWALL_APP_CONTAINER structure


## -description


The <b>INET_FIREWALL_APP_CONTAINER</b> structure contains information about an specific app container.
<div class="code"></div>

## -struct-fields




### -field appContainerSid

Type: <b>SID*</b>

The package identifier of the app container


### -field userSid

Type: <b>SID*</b>

The security identifier (SID) of the user to whom the app container belongs.


### -field appContainerName

Type: <b>LPWSTR</b>

The app container's globally unique name.

 Also referred to as the  Package Family Name, for the app container of a Windows Store app.


### -field displayName

Type: <b>LPWSTR</b>

Friendly name of the app container


### -field description

Type: <b>LPWSTR</b>

A description of the app container (its use, the objective of the application that uses it, etc.)


### -field capabilities

Type: <b><a href="https://msdn.microsoft.com/37386225-0c64-49c0-a21c-cecd8bdb1f1f">INET_FIREWALL_AC_CAPABILITIES</a></b>

The capabilities of the app container.


### -field binaries

Type: <b><a href="https://msdn.microsoft.com/5403303e-e65c-47cf-af84-3d748db8661b">INET_FIREWALL_AC_BINARIES</a></b>

Binary paths to the applications running in the app container.


### -field workingDirectory

 


### -field packageFullName

 




## -see-also




<a href="https://msdn.microsoft.com/5403303e-e65c-47cf-af84-3d748db8661b">INET_FIREWALL_AC_BINARIES</a>



<a href="https://msdn.microsoft.com/37386225-0c64-49c0-a21c-cecd8bdb1f1f">INET_FIREWALL_AC_CAPABILITIES</a>
 

 

