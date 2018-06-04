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

# FOLDERVIEWOPTIONS enumeration


## -description


Used by methods of the <a href="https://msdn.microsoft.com/4831e62c-45e4-435d-b926-0e140cbfb6fc">IFolderViewOptions</a> interface to activate Windows Vista options not supported by default in Windows 7 and later systems as well as deactivating new Windows 7 options.


## -enum-fields




### -field FVO_DEFAULT

0x00000000. Do not use any special options.


### -field FVO_VISTALAYOUT

0x00000001. Use the Windows Vista list view. This can be used to maintain continuity between systems so that users are presented with an expected view. At this time, setting this flag has the effective, though not literal, result of the application of the FVO_CUSTOMPOSITION and FVO_CUSTOMORDERING flags. However, this could change. Applications should be specific about the behaviors that they require. For instance, if an application requires custom positioning of its items, it should not rely on FVO_VISTALAYOUT to provide it, but instead explicitly apply the FVO_CUSTOMPOSITION flag.


### -field FVO_CUSTOMPOSITION

0x00000002. Items require custom positioning within the space of the view. Those items are positioned to specific coordinates. This option is not active by default in the Windows 7 view.


### -field FVO_CUSTOMORDERING

0x00000004. Items require custom ordering within the view. This option is not active by default in the Windows 7 view. When it is active, the user can reorder the view by dragging items to their desired locations.


### -field FVO_SUPPORTHYPERLINKS

0x00000008. Tiles and Details displays can contain hyperlinks. This option is not active by default in the Windows 7 view. When hyperlinks are displayed, they are updated to the Windows 7 view.


### -field FVO_NOANIMATIONS

0x00000010. Do not display animations in the view. This option was introduced in Windows 7 and is active by default in the Windows 7 view.


### -field FVO_NOSCROLLTIPS

0x00000010. Do not show scroll tips. This option was introduced in Windows 7 and is active by default in the Windows 7 view.



A scroll tip displays the names of files as they are scrolled past, as a visual clue to your location in the list. An example is shown here.

<img alt="Screen shot of a Scroll tip displaying the name of the Shell32.dll file in the System32 folder." src="images/scrolltip.jpg"/>

