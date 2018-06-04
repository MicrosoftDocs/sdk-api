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

# _SPBEGINF enumeration


## -description


Used by <a href="https://msdn.microsoft.com/c26dd072-6d59-4c6c-a273-682ded994612">IActionProgress::Begin</a>, these constants specify certain UI operations that are to be enabled or disabled.


## -enum-fields




### -field SPBEGINF_NORMAL

Indicates default progress behavior.


### -field SPBEGINF_AUTOTIME

Indicates that the progress UI should automatically update a text field with the amount of time remaining until the action completes.


### -field SPBEGINF_NOPROGRESSBAR

Indicates that the UI should not display a progress bar.


### -field SPBEGINF_MARQUEEPROGRESS

Indicates that the UI should use a marquee-style progress bar.


### -field SPBEGINF_NOCANCELBUTTON

Indicates that the UI should not include a <b>Cancel</b> button.


## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/c26dd072-6d59-4c6c-a273-682ded994612">IActionProgress::Begin</a>
 

 

