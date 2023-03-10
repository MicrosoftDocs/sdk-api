---
UID: NF:uiautomationcoreapi.ScrollItemPattern_ScrollIntoView
title: ScrollItemPattern_ScrollIntoView function (uiautomationcoreapi.h)
description: Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.
helpviewer_keywords: ["ScrollItemPattern_ScrollIntoView","ScrollItemPattern_ScrollIntoView function [Windows Accessibility]","uiauto.uiauto_ScrollItemPattern_ScrollIntoViewConPat","uiauto_ScrollItemPattern_ScrollIntoViewConPat","uiautomationcoreapi/ScrollItemPattern_ScrollIntoView","winauto.uiauto_ScrollItemPattern_ScrollIntoViewConPat"]
old-location: winauto\uiauto_ScrollItemPattern_ScrollIntoViewConPat.htm
tech.root: WinAuto
ms.assetid: cd68138f-dcd2-4d1d-aee6-f25168b0045b
ms.date: 12/05/2018
ms.keywords: ScrollItemPattern_ScrollIntoView, ScrollItemPattern_ScrollIntoView function [Windows Accessibility], uiauto.uiauto_ScrollItemPattern_ScrollIntoViewConPat, uiauto_ScrollItemPattern_ScrollIntoViewConPat, uiautomationcoreapi/ScrollItemPattern_ScrollIntoView, winauto.uiauto_ScrollItemPattern_ScrollIntoViewConPat
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ScrollItemPattern_ScrollIntoView
 - uiautomationcoreapi/ScrollItemPattern_ScrollIntoView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - ScrollItemPattern_ScrollIntoView
---

# ScrollItemPattern_ScrollIntoView function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Scrolls the content area of a container object in order to display the UI Automation element within the visible region (viewport) of the container.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

This method does not guarantee the position of the UI Automation element 
            within the visible region (viewport) of the container.