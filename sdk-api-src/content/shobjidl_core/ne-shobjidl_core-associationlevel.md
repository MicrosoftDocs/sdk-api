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

# ASSOCIATIONLEVEL enumeration


## -description


Specifies the source of the default association for a file name extension. Used by methods of the <a href="https://msdn.microsoft.com/015a3be4-2e74-4a2b-8c02-54dcbf0ecacd">IApplicationAssociationRegistration</a> interface.


## -enum-fields




### -field AL_MACHINE

The machine-level default application association.


### -field AL_EFFECTIVE

The effective default for the current user. This value should be used by most applications.


### -field AL_USER

The per-user default application association. If this value is used and no per-user default is declared, the calling method fails with a value of <code>HRESULT_FROM_WIN32(ERROR_NO_ASSOCIATION)</code>.


## -see-also




<a href="https://msdn.microsoft.com/40e6f80d-a778-4d5f-bb1b-db294815f8b5">HRESULT_FROM_WIN32</a>
 

 

