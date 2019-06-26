---
UID: NF:uiautomationcoreapi.ScrollPattern_Scroll
title: ScrollPattern_Scroll function (uiautomationcoreapi.h)
author: windows-sdk-content
description: Scrolls the currently visible region of the content area the specified ScrollAmount, horizontally, vertically, or both.
old-location: winauto\uiauto_ScrollPattern_ScrollConPat.htm
tech.root: WinAuto
ms.assetid: fffed882-89db-47f1-8e3a-a2c8e11ac865
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ScrollPattern_Scroll, ScrollPattern_Scroll function [Windows Accessibility], uiauto.uiauto_ScrollPattern_ScrollConPat, uiauto_ScrollPattern_ScrollConPat, uiautomationcoreapi/ScrollPattern_Scroll, winauto.uiauto_ScrollPattern_ScrollConPat
ms.topic: function
f1_keywords: 
 - "uiautomationcoreapi/ScrollPattern_Scroll"
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ScrollPattern_Scroll function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Scrolls the currently visible region of the content area the specified <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a>, horizontally, 
        vertically, or both.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param horizontalAmount [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a></b>

The amount to scroll the container on the horizontal axis, as a percentage.


### -param verticalAmount [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a></b>

The amount to scroll the container on the vertical axis, as a percentage.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



