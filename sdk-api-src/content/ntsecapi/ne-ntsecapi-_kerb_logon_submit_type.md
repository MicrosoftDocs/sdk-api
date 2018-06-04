---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _KERB_LOGON_SUBMIT_TYPE enumeration


## -description


The <b>KERB_LOGON_SUBMIT_TYPE</b> enumeration identifies the type of logon being requested.


## -enum-fields




### -field KerbInteractiveLogon

Perform an interactive logon.


### -field KerbSmartCardLogon

Logon using a smart card.


### -field KerbWorkstationUnlockLogon

Unlock a workstation.


### -field KerbSmartCardUnlockLogon

Unlock a workstation using a smart card.


### -field KerbProxyLogon

Logon using a proxy server.


### -field KerbTicketLogon

Logon using a valid <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> ticket as a credential.


### -field KerbTicketUnlockLogon

Unlock a workstation by using a Kerberos ticket.


### -field KerbS4ULogon

Perform a service for user logon.


### -field KerbCertificateLogon

Logon interactively using a certificate stored on a smart card.


### -field KerbCertificateS4ULogon

Perform a service for user logon using a certificate stored on a smart card.


### -field KerbCertificateUnlockLogon

Unlock a workstation using a certificate stored on a smart card.


### -field KerbNoElevationLogon


### -field KerbLuidLogon



