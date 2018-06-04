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

# _MSA_INFO_STATE enumeration


## -description


Indicates the state of a managed service account. A managed service account  can be  either a group managed service account (gMSA) or a standalone managed service account (sMSA). A sMSA is limited to being deployed to a single computer.


## -enum-fields




### -field MsaInfoNotExist

The account does not exist.


### -field MsaInfoNotService

The account exists, but it is not a group managed service account (gMSA) or a Windows Server 2008 R2 or Windows 7 managed service account.

<b>Windows Server 2008 R2 and Windows 7:  </b> The account is not a managed service account.


### -field MsaInfoCannotInstall

If the managed service account is a gMSA, the credentials cannot be fetched from the active directory or the Kerberos encryption types did not match.

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account cannot be installed.


### -field MsaInfoCanInstall

The sMSA can be installed. This constant will never be returned for a gMSA. 

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account can be installed.


### -field MsaInfoInstalled

The gMSA managed service account is installed.

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account is installed.


## -remarks



Service accounts  can be group managed and are called group managed service accounts (gMSA). Standalone managed service accounts (sMSA) are limited to being deployed to a single computer.

<b>Windows Server 2008 R2 and Windows 7:  </b> The managed service account (MSA) is limited to being deployed to a single computer.




## -see-also




<a href="https://msdn.microsoft.com/21e04ee8-98c9-4c78-9564-e07f5edaf847">MSA_INFO_0</a>
 

 

