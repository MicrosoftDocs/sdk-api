---
UID: NF:uiautomationcoreapi.TextRange_ScrollIntoView
title: TextRange_ScrollIntoView function
author: windows-sdk-content
description: Scrolls the text so the specified range is visible in the viewport.
old-location: winauto\uiauto_TextRange_ScrollIntoViewConPat.htm
old-project: WinAuto
ms.assetid: 94c922ba-7f43-4881-b876-c77fdf7b9eb5
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: TextRange_ScrollIntoView, TextRange_ScrollIntoView function [Windows Accessibility], uiauto.uiauto_TextRange_ScrollIntoViewConPat, uiauto_TextRange_ScrollIntoViewConPat, uiautomationcoreapi/TextRange_ScrollIntoView, winauto.uiauto_TextRange_ScrollIntoViewConPat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - TextRange_ScrollIntoView
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TextRange_ScrollIntoView function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Scrolls the text so the specified range is visible in the viewport.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range to scroll.


### -param alignToTop [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

TRUE to align the top of the text range with the top of the viewport; 
				FALSE to align the bottom of the text range with the bottom of the viewport.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



