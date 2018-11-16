---
UID: NF:icm.SetupColorMatchingW
title: SetupColorMatchingW function
author: windows-sdk-content
description: The SetupColorMatching function creates a Color Management dialog box that lets the user choose whether to enable color management, and if so, provides control over the color profiles used and over the rendering intent.
old-location: wcs\setupcolormatching.htm
tech.root: WCS
ms.assetid: 7d3b6d3f-49f4-46f5-a43b-868e53965d8f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SetupColorMatching, SetupColorMatching function [Windows Color System], SetupColorMatchingA, SetupColorMatchingW, _color_SetupColorMatching, icm/SetupColorMatching, icm/SetupColorMatchingA, icm/SetupColorMatchingW, wcs.setupcolormatching
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupColorMatchingW (Unicode) and SetupColorMatchingA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Icmui.lib
req.dll: Icmui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icmui.dll
api_name:
 - SetupColorMatching
 - SetupColorMatchingA
 - SetupColorMatchingW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetupColorMatchingW
: 
---

# SetupColorMatchingW function


## -description


The <b>SetupColorMatching</b> function creates a Color Management dialog box that lets the user choose whether to enable color management, and if so, provides control over the color profiles used and over the <a href="r.htm">rendering intent</a>.


## -parameters




### -param pcms

Pointer to a <a href="https://msdn.microsoft.com/920c9ac2-bb77-4805-9345-15611db1aade">COLORMATCHSETUP</a> structure that on entry contains information used to initialize the dialog box.

When <b>SetupColorMatching</b> returns, if the user clicked the OK button, this structure contains information about the user's selection. Otherwise, if an error occurred or the user canceled the dialog box, the structure is left unchanged.


## -returns



If this function succeeds, the return value is <b>TRUE</b> indicating that no errors occurred and the user clicked the OK button.

If this function fails, the return value is <b>FALSE</b> indicating that an error occurred or the dialog was canceled. For extended error information, call <b>GetLastError</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

