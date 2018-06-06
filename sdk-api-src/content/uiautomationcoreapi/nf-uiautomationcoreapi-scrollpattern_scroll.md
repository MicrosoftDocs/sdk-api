---
UID: NF:uiautomationcoreapi.ScrollPattern_Scroll
title: ScrollPattern_Scroll function
author: windows-sdk-content
description: Scrolls the currently visible region of the content area the specified ScrollAmount, horizontally, vertically, or both.
old-location: winauto\uiauto_ScrollPattern_ScrollConPat.htm
old-project: WinAuto
ms.assetid: fffed882-89db-47f1-8e3a-a2c8e11ac865
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: ScrollPattern_Scroll, ScrollPattern_Scroll function [Windows Accessibility], uiauto.uiauto_ScrollPattern_ScrollConPat, uiauto_ScrollPattern_ScrollConPat, uiautomationcoreapi/ScrollPattern_Scroll, winauto.uiauto_ScrollPattern_ScrollConPat
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
 - ScrollPattern_Scroll
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ScrollPattern_Scroll function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Scrolls the currently visible region of the content area the specified <a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a>, horizontally, 
        vertically, or both.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param horizontalAmount [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

The amount to scroll the container on the horizontal axis, as a percentage.


### -param verticalAmount [in]

Type: <b><a href="https://msdn.microsoft.com/94d84a66-5222-48e4-9675-444eb04558a4">ScrollAmount</a></b>

The amount to scroll the container on the vertical axis, as a percentage.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



