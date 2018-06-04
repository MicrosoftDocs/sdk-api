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

# ENTERPRISE_DATA_POLICIES enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]


<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Indicates whether the app is enlightened for Windows Information Protection (WIP) and whether the app is managed by policy. 


## -enum-fields




### -field ENTERPRISE_POLICY_NONE

The app is not managed by enterprise policy.


### -field ENTERPRISE_POLICY_ALLOWED

The app is allowed to access enterprise resources according to the enterprise policy.


### -field ENTERPRISE_POLICY_ENLIGHTENED

The app is enlightened (self-declared in the app's resource file).


### -field ENTERPRISE_POLICY_EXEMPT

The app is marked as exempt by the enterprise policy.

