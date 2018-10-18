---
UID: NE:shobjidl.FOLDERVIEWOPTIONS
title: FOLDERVIEWOPTIONS
author: windows-sdk-content
description: Used by methods of the IFolderViewOptions interface to activate Windows Vista options not supported by default in Windows 7 and later systems as well as deactivating new Windows 7 options.
old-location: shell\FOLDERVIEWOPTIONS.htm
tech.root: shell
ms.assetid: ab0ebc82-e917-4e3a-864b-fc3bb6280a48
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: FOLDERVIEWOPTIONS, FOLDERVIEWOPTIONS enumeration [Windows Shell], FVO_CUSTOMORDERING, FVO_CUSTOMPOSITION, FVO_DEFAULT, FVO_NOANIMATIONS, FVO_NOSCROLLTIPS, FVO_SUPPORTHYPERLINKS, FVO_VISTALAYOUT, _shell_FOLDERVIEWOPTIONS, shell.FOLDERVIEWOPTIONS, shobjidl/FOLDERVIEWOPTIONS, shobjidl/FVO_CUSTOMORDERING, shobjidl/FVO_CUSTOMPOSITION, shobjidl/FVO_DEFAULT, shobjidl/FVO_NOANIMATIONS, shobjidl/FVO_NOSCROLLTIPS, shobjidl/FVO_SUPPORTHYPERLINKS, shobjidl/FVO_VISTALAYOUT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl.h
api_name:
 - FOLDERVIEWOPTIONS
product: Windows
targetos: Windows
req.typenames: FOLDERVIEWOPTIONS
req.redist: 
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

