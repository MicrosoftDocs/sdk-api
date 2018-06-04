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

# PolicyServerUrlFlags enumeration


## -description


The <b>PolicyServerUrlFlags</b> enumeration contains certificate enrollment policy (CEP) server flags. It is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method on the <a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a> interface.


## -enum-fields




### -field PsfNone

No flags are specified.


### -field PsfLocationGroupPolicy

Policy information is specified in group policy by an administrator.


### -field PsfLocationRegistry

Policy information is specified in the registry.


### -field PsfUseClientId

Specifies that certificate enrollments and renewals include client specific data in a <b>ClientId</b> attribute. Examples include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name. This flag can be set by group policy.

This flag has been included to address privacy concerns that can arise during enrollment to servers that are managed by administrators other than those who manage the forest in which the user resides. By not setting this flag, you can prevent sending personal information to non-local administrators.


### -field PsfAutoEnrollmentEnabled

Automatic certificate enrollment is enabled.


### -field PsfAllowUnTrustedCA

Specifies that the certificate of the issuing CA need not be trusted by the client to install a certificate signed by the CA.


## -see-also




<a href="https://msdn.microsoft.com/1af7b178-3226-43c3-bfbe-08738f9ef851">ICertPropertyEnrollmentPolicyServer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
 

 

