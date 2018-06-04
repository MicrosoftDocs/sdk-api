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

# ListView_SetIconSpacing macro


## -description


Sets the spacing between icons in list-view controls set to the <a href="List_view_window_styles.htm">LVS_ICON</a> style. You can use this macro or send the <a href="https://msdn.microsoft.com/2dd3d9df-5b0d-445e-9201-d766fa218f90">LVM_SETICONSPACING</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param cx

Type: <b>int</b>

The distance, in pixels, to set between icons on the x-axis. 


### -param cy

Type: <b>int</b>

The distance, in pixels, to set between icons on the y-axis. 


## -remarks



The 
				<i>cx</i> and <i>cy</i> parameters are relative to the upper-left corner of an icon bitmap. Therefore, to set spacing between icons that do not overlap, the <i>cx</i> or <i>cy</i> values must include the size of the icon, plus the amount of empty space desired between icons. Values that do not include the width of the icon will result in overlaps.

When defining the icon spacing, <i>cx</i> and <i>cy</i> must set to 4 or larger. Smaller values will not yield the desired layout. You can reset <i>cx</i> and <i>cy</i> to the default spacing by setting both values to -1. This approach only allows you to reset both default settings. You cannot reset only <i>cx</i> or <i>cy</i> to the default setting by setting one of them to -1.



