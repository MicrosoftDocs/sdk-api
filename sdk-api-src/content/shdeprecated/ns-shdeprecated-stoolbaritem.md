---
UID: NS:shdeprecated.SToolbarItem
title: SToolbarItem
author: windows-driver-content
description: Deprecated. Data used in IBrowserService2::_GetToolbarItem, IBrowserService2::v_MayGetNextToolbarFocus, and IBrowserService2::_SetFocus to define a toolbar item.
old-location: shell\TOOLBARITEM.htm
old-project: shell
ms.assetid: 7378f2f3-c164-46fe-9989-a7a57fceb48a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*LPTOOLBARITEM, LPTOOLBARITEM, LPTOOLBARITEM structure pointer [Windows Shell], SToolbarItem, TOOLBARITEM, TOOLBARITEM structure [Windows Shell], _shell_TOOLBARITEM, shdeprecated/LPTOOLBARITEM, shdeprecated/TOOLBARITEM, shell.TOOLBARITEM"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TOOLBARITEM, *LPTOOLBARITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Shdeprecated.h
api_name:
-	TOOLBARITEM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# SToolbarItem structure


## -description


Deprecated. Data used in <a href="https://msdn.microsoft.com/9bce71ca-189e-4072-9acf-10c8b3a34c5c">IBrowserService2::_GetToolbarItem</a>, <a href="https://msdn.microsoft.com/a1c271b2-d567-43b4-966e-0eea597f004b">IBrowserService2::v_MayGetNextToolbarFocus</a>, and <a href="https://msdn.microsoft.com/4a69c3f4-49e0-4a06-8cf2-dc8db640f58f">IBrowserService2::_SetFocus</a> to define a toolbar item.


## -struct-fields




### -field ptbar

Type: <b><a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a>*</b>

The <a href="https://msdn.microsoft.com/9e80fd5e-f57d-4801-b198-73b8f5ffff6e">IDockingWindow</a> of the item's particular toolbar.


### -field rcBorderTool

Type: <b><a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a></b>

A <a href="https://msdn.microsoft.com/f86321d9-5706-4641-b3c9-981a8acacff6">BORDERWIDTHS</a> structure that contains the dimensions of the item, including its borders.


### -field pwszItem

Type: <b>LPWSTR</b>

A pointer to a buffer that contains the name of the toolbar item as a Unicode string.


### -field fShow

Type: <b>BOOL</b>

<b>TRUE</b> if the toolbar item is currently visible; otherwise, <b>FALSE</b>.


### -field hMon

Type: <b>HMONITOR</b>

The handle of the monitor on which the toolbar item appears.

