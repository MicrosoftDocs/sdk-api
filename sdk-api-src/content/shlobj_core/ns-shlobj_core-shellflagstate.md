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

# SHELLFLAGSTATE structure


## -description


Contains a set of flags that indicate the current Shell settings. This structure is used with the <a href="https://msdn.microsoft.com/728a4004-f35d-4592-baf1-456a613a3344">SHGetSettings</a> function.


## -struct-fields




### -field fShowAllObjects

Type: <b>BOOL</b>

Nonzero if the <b>Show All Files</b> option is enabled, or zero otherwise.


### -field fShowExtensions

Type: <b>BOOL</b>

Nonzero if the <b>Hide extensions for known file types</b> option is disabled, or zero otherwise.


### -field fNoConfirmRecycle

Type: <b>BOOL</b>

Nonzero if the <b>Display Delete Confirmation Dialog</b> box in the Recycle Bin is enabled, or zero otherwise.


### -field fShowSysFiles

Type: <b>BOOL</b>

Nonzero if the <b>Don't show hidden files, folders, or drives</b> option is selected, or zero otherwise.


### -field fShowCompColor

Type: <b>BOOL</b>

Nonzero if the <b>Display encrypted or compressed NTFS files in color</b> option is enabled, or zero otherwise.


### -field fDoubleClickInWebView

Type: <b>BOOL</b>

Nonzero if the <b>Double-Click to Open an Item</b> option is enabled, or zero otherwise.


### -field fDesktopHTML

Type: <b>BOOL</b>

Nonzero if the <b>Active Desktop – View as Web Page</b> option is enabled, or zero otherwise.


### -field fWin95Classic

Type: <b>BOOL</b>

Nonzero if the <b>Classic Style</b> option is enabled, or zero otherwise.


### -field fDontPrettyPath

Type: <b>BOOL</b>

Nonzero if the <b>Allow All Uppercase Names</b> option is enabled, or zero otherwise.


### -field fShowAttribCol

Type: <b>BOOL</b>

Nonzero if the <b>Show File Attributes in Detail View</b> option is enabled, or zero otherwise. 
                    

<b>Windows Vista and later</b>. Not used.


### -field fMapNetDrvBtn

Type: <b>BOOL</b>

Nonzero if the <b>Show Map Network Drive Button in Toolbar</b> option is enabled, or zero otherwise.


### -field fShowInfoTip

Type: <b>BOOL</b>

Nonzero if the <b>Show Info Tips for Items in Folders &amp; Desktop</b> option is enabled, or zero otherwise.


### -field fHideIcons

Type: <b>BOOL</b>

Nonzero if the <b>Show Desktop Icons</b> option is enabled, or zero otherwise.


### -field fAutoCheckSelect

Type: <b>BOOL</b>

<b>Windows Vista and later</b>: Nonzero if the <b>Use checkboxes to select  items</b> option is enabled, or zero otherwise.


### -field fIconsOnly

Type: <b>BOOL</b>

<b>Windows Vista and later</b>: Nonzero if the <b>Always show icons, never thumbnails</b> option is enabled, or zero otherwise.


### -field fRestFlags

Type: <b>UINT</b>

For Windows Vista this bitfield is 1, otherwise member this is not used.

