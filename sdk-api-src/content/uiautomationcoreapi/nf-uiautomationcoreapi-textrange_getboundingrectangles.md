---
UID: NF:uiautomationcoreapi.TextRange_GetBoundingRectangles
title: TextRange_GetBoundingRectangles function
author: windows-driver-content
description: Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.
old-location: winauto\uiauto_TextRange_GetBoundingRectanglesConPat.htm
old-project: WinAuto
ms.assetid: f6b9e6b5-554d-46cb-a423-e7e3f6fb3a04
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: TextRange_GetBoundingRectangles, TextRange_GetBoundingRectangles function [Windows Accessibility], uiauto.uiauto_TextRange_GetBoundingRectanglesConPat, uiauto_TextRange_GetBoundingRectanglesConPat, uiautomationcoreapi/TextRange_GetBoundingRectangles, winauto.uiauto_TextRange_GetBoundingRectanglesConPat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
api_name:
-	TextRange_GetBoundingRectangles
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TextRange_GetBoundingRectangles function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the minimum number of bounding rectangles that can enclose the range, one rectangle per line.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.


### -param pRetVal [out]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

When this function returns, contains 
				an array of rectangle coordinates for the lines of text that the range spans. 
				This parameter is passed uninitialized.
				The SAFEARRAY contains VARIANTs of type VT_I4.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



