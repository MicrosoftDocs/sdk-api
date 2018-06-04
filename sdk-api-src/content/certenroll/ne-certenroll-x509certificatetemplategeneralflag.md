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

# X509CertificateTemplateGeneralFlag enumeration


## -description


The <b>X509CertificateTemplateGeneralFlag</b> enumeration contains use and modification information about templates and associated certificates.


## -enum-fields




### -field GeneralMachineType

The template should be used to create a certificate request for a computer.


### -field GeneralCA

The template should be used to create a request for a certification authority certificate.


### -field GeneralCrossCA

The template should be used to create a request to cross certify a certificate.


### -field GeneralDefault

The template is not used by the client or server in the Windows Client Certificate Enrollment and should not be modified.


### -field GeneralModified

The template is not used by the client or server in the Windows Client Certificate Enrollment and can be modified if necessary.


### -field GeneralDonotPersist

The certification authority is not required to save a record of a certificate request for a certificate that has been issued.

