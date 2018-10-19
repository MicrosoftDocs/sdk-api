---
UID: NS:uxtheme._BP_ANIMATIONPARAMS
title: "_BP_ANIMATIONPARAMS"
author: windows-sdk-content
description: Defines animation parameters for the BP_PAINTPARAMS structure used by BeginBufferedPaint.
old-location: controls\BP_ANIMATIONPARAMS.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\structures\bp_animationparams.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PBP_ANIMATIONPARAMS, BP_ANIMATIONPARAMS, BP_ANIMATIONPARAMS structure [Windows Controls], PBP_ANIMATIONPARAMS, PBP_ANIMATIONPARAMS structure pointer [Windows Controls], _BP_ANIMATIONPARAMS, _shell_BP_ANIMATIONPARAMS, _shell_BP_ANIMATIONPARAMS_cpp, controls.BP_ANIMATIONPARAMS, controls._shell_BP_ANIMATIONPARAMS, uxtheme/BP_ANIMATIONPARAMS, uxtheme/PBP_ANIMATIONPARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Uxtheme.h
api_name:
 - BP_ANIMATIONPARAMS
product: Windows
targetos: Windows
req.typenames: BP_ANIMATIONPARAMS, *PBP_ANIMATIONPARAMS
req.redist: 
---

# _BP_ANIMATIONPARAMS structure


## -description


Defines animation parameters for the <a href="https://msdn.microsoft.com/en-us/library/Bb773228(v=VS.85).aspx">BP_PAINTPARAMS</a> structure used by <a href="https://msdn.microsoft.com/en-us/library/Bb773257(v=VS.85).aspx">BeginBufferedPaint</a>.


## -struct-fields




### -field cbSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The size, in bytes, of this structure.


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Reserved. 


### -field style

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb759833(v=VS.85).aspx">BP_ANIMATIONSTYLE</a></b>

Animation style.


### -field dwDuration

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Length of the animation, in milliseconds.

