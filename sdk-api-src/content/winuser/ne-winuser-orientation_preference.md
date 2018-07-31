---
UID: NE:winuser.ORIENTATION_PREFERENCE
title: ORIENTATION_PREFERENCE
author: windows-sdk-content
description: Indicates the screen orientation preference for a desktop app process.
old-location: base\orientation_preference.htm
old-project: ProcThread
ms.assetid: 7399DD9F-F993-40CC-B9C6-20673D39C069
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ORIENTATION_PREFERENCE, ORIENTATION_PREFERENCE enumeration, ORIENTATION_PREFERENCE_LANDSCAPE, ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED, ORIENTATION_PREFERENCE_NONE, ORIENTATION_PREFERENCE_PORTRAIT, ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED, base.orientation_preference, winuser/ORIENTATION_PREFERENCE, winuser/ORIENTATION_PREFERENCE_LANDSCAPE, winuser/ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED, winuser/ORIENTATION_PREFERENCE_NONE, winuser/ORIENTATION_PREFERENCE_PORTRAIT, winuser/ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winuser.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: ORIENTATION_PREFERENCE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinUser.h
api_name:
 - ORIENTATION_PREFERENCE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ORIENTATION_PREFERENCE enumeration


## -description


Indicates the screen orientation preference for a desktop app process.


## -enum-fields




### -field ORIENTATION_PREFERENCE_NONE

The process has no device orientation preferences. The system may choose any available setting.


### -field ORIENTATION_PREFERENCE_LANDSCAPE

The process represents a desktop app that can be used in landscape mode.


### -field ORIENTATION_PREFERENCE_PORTRAIT

The process represents a desktop app that can be used in portrait mode.


### -field ORIENTATION_PREFERENCE_LANDSCAPE_FLIPPED

 The process represents a desktop app that can be used in flipped landscape mode.


### -field ORIENTATION_PREFERENCE_PORTRAIT_FLIPPED

The process represents a desktop app that can be used in flipped portrait mode.

