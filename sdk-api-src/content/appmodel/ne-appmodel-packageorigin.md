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

# PackageOrigin enumeration


## -description


Specifies the origin of a package. 


## -enum-fields




### -field PackageOrigin_Unknown

The package's origin is unknown.


### -field PackageOrigin_Unsigned

The package originated as unsigned.


### -field PackageOrigin_Inbox

The package was included inbox.


### -field PackageOrigin_Store

The package originated from the Windows Store. 


### -field PackageOrigin_DeveloperUnsigned

The package originated as developer unsigned.


### -field PackageOrigin_DeveloperSigned

The package originated as developer signed.


### -field PackageOrigin_LineOfBusiness

The package originated as a line-of-business app.


## -see-also




<a href="https://msdn.microsoft.com/7A1EE2CA-83CE-4E03-85A5-0061E29EB49B">GetStagedPackageOrigin</a>
 

 

