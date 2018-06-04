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

# STPFLAG enumeration


## -description


Used by the <a href="https://msdn.microsoft.com/cc3fec4b-7770-44af-9892-239a17dd96b8">ITaskbarList4::SetTabProperties</a> method to specify tab properties.


## -enum-fields




### -field STPF_NONE

No specific property values are specified. The default behavior is used: the tab window provides a thumbnail and peek image, either live or static as appropriate.


### -field STPF_USEAPPTHUMBNAILALWAYS

Always use the thumbnail provided by the main application frame window rather than a thumbnail provided by the individual tab window. Do not combine this value with STPF_USEAPPTHUMBNAILWHENACTIVE; doing so will result in an error.


### -field STPF_USEAPPTHUMBNAILWHENACTIVE

When the application tab is active and a live representation of its window is available, use the main application's frame window thumbnail. At other times, use the tab window thumbnail. Do not combine this value with STPF_USEAPPTHUMBNAILALWAYS; doing so will result in an error.


### -field STPF_USEAPPPEEKALWAYS

Always use the peek image provided by the main application frame window rather than a peek image provided by the individual tab window. Do not combine this value with STPF_USEAPPPEEKWHENACTIVE; doing so will result in an error.


### -field STPF_USEAPPPEEKWHENACTIVE

When the application tab is active and a live representation of its window is available, show the main application frame in the peek feature. At other times, use the tab window. Do not combine this value with STPF_USEAPPPEEKALWAYS; doing so will result in an error.

