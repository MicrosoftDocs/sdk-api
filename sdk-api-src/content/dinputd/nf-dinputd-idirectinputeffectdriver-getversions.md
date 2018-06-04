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

# IDirectInputEffectDriver::GetVersions


## -description


The <b>IDirectInputEffectDriver::GetVersions </b>method obtains version information about the force-feedback hardware and driver. 


## -parameters






#### - pvers

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538438">DIDRIVERVERSIONS</a> structure that should be filled in with version information describing the hardware, firmware, and driver. DirectInput sets the <b>dwSize</b> member of the DIDRIVERVERSIONS structure to <b>sizeof</b>(DIDRIVERVERSIONS) before calling this method. 


## -returns



Returns S_OK if successful; otherwise, returns an error code.



