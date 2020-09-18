---
UID: NS:uxtheme._BP_ANIMATIONPARAMS
title: BP_ANIMATIONPARAMS (uxtheme.h)
description: Defines animation parameters for the BP_PAINTPARAMS structure used by BeginBufferedPaint.
helpviewer_keywords: ["*PBP_ANIMATIONPARAMS","BP_ANIMATIONPARAMS","BP_ANIMATIONPARAMS structure [Windows Controls]","PBP_ANIMATIONPARAMS","PBP_ANIMATIONPARAMS structure pointer [Windows Controls]","_shell_BP_ANIMATIONPARAMS","_shell_BP_ANIMATIONPARAMS_cpp","controls.BP_ANIMATIONPARAMS","controls._shell_BP_ANIMATIONPARAMS","uxtheme/BP_ANIMATIONPARAMS","uxtheme/PBP_ANIMATIONPARAMS"]
old-location: controls\BP_ANIMATIONPARAMS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\structures\bp_animationparams.htm
ms.date: 12/05/2018
ms.keywords: '*PBP_ANIMATIONPARAMS, BP_ANIMATIONPARAMS, BP_ANIMATIONPARAMS structure [Windows Controls], PBP_ANIMATIONPARAMS, PBP_ANIMATIONPARAMS structure pointer [Windows Controls], _shell_BP_ANIMATIONPARAMS, _shell_BP_ANIMATIONPARAMS_cpp, controls.BP_ANIMATIONPARAMS, controls._shell_BP_ANIMATIONPARAMS, uxtheme/BP_ANIMATIONPARAMS, uxtheme/PBP_ANIMATIONPARAMS'
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
targetos: Windows
req.typenames: BP_ANIMATIONPARAMS, *PBP_ANIMATIONPARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BP_ANIMATIONPARAMS
 - uxtheme/_BP_ANIMATIONPARAMS
 - PBP_ANIMATIONPARAMS
 - uxtheme/PBP_ANIMATIONPARAMS
 - BP_ANIMATIONPARAMS
 - uxtheme/BP_ANIMATIONPARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Uxtheme.h
api_name:
 - BP_ANIMATIONPARAMS
---

# BP_ANIMATIONPARAMS structure


## -description

Defines animation parameters for the <a href="/windows/desktop/api/uxtheme/ns-uxtheme-bp_paintparams">BP_PAINTPARAMS</a> structure used by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The size, in bytes, of this structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Reserved.

### -field style

Type: <b><a href="/windows/desktop/api/uxtheme/ne-uxtheme-bp_animationstyle">BP_ANIMATIONSTYLE</a></b>

Animation style.

### -field dwDuration

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Length of the animation, in milliseconds.