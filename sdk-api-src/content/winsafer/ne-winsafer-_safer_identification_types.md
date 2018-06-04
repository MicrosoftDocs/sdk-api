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

# _SAFER_IDENTIFICATION_TYPES enumeration


## -description


The <b>SAFER_IDENTIFICATION_TYPES</b> enumeration type defines the possible types of identification rule structures that can be identified by the  <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure.


## -enum-fields




### -field SaferIdentityDefault

The header is for a default level structure.


### -field SaferIdentityTypeImageName

The header is for a <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a> structure.


### -field SaferIdentityTypeImageHash

The header is for a <a href="https://msdn.microsoft.com/68b4b5f5-8220-4180-8243-b6f1fd7826bd">SAFER_HASH_IDENTIFICATION</a> structure.


### -field SaferIdentityTypeUrlZone

The header is for a <a href="https://msdn.microsoft.com/8f165956-9ef0-469e-a71b-f9341a347e59">SAFER_URLZONE_IDENTIFICATION</a> structure.


### -field SaferIdentityTypeCertificate

The header is for a <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a> structure.


## -remarks



The <b>SAFER_IDENTIFICATION_TYPES</b> enumeration type is used by the <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure.



