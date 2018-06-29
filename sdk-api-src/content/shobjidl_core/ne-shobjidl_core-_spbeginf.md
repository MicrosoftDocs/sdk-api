---
UID: NE:shobjidl_core._SPBEGINF
title: "_SPBEGINF"
author: windows-sdk-content
description: Used by IActionProgress::Begin, these constants specify certain UI operations that are to be enabled or disabled.
old-location: shell\SPBEGINF_Constants.htm
old-project: shell
ms.assetid: dc5215ca-17c8-47c1-8059-f46400ff1d0f
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: SPBEGINF, SPBEGINF enumeration [Windows Shell], SPBEGINF_AUTOTIME, SPBEGINF_MARQUEEPROGRESS, SPBEGINF_NOCANCELBUTTON, SPBEGINF_NOPROGRESSBAR, SPBEGINF_NORMAL, _SPBEGINF, shell.SPBEGINF_Constants, shell_SPBEGINF_Constants, shobjidl_core/SPBEGINF, shobjidl_core/SPBEGINF_AUTOTIME, shobjidl_core/SPBEGINF_MARQUEEPROGRESS, shobjidl_core/SPBEGINF_NOCANCELBUTTON, shobjidl_core/SPBEGINF_NOPROGRESSBAR, shobjidl_core/SPBEGINF_NORMAL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SPBEGINF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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
 

 

