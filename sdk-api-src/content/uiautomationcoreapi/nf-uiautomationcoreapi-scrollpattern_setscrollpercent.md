---
UID: NF:uiautomationcoreapi.ScrollPattern_SetScrollPercent
title: ScrollPattern_SetScrollPercent function (uiautomationcoreapi.h)
description: Scrolls a container to a specific position horizontally, vertically, or both.
helpviewer_keywords: ["ScrollPattern_SetScrollPercent","ScrollPattern_SetScrollPercent function [Windows Accessibility]","uiauto.uiauto_ScrollPattern_SetScrollPercentConPat","uiauto_ScrollPattern_SetScrollPercentConPat","uiautomationcoreapi/ScrollPattern_SetScrollPercent","winauto.uiauto_ScrollPattern_SetScrollPercentConPat"]
old-location: winauto\uiauto_ScrollPattern_SetScrollPercentConPat.htm
tech.root: WinAuto
ms.assetid: 5a152e0b-f1c2-41c7-add6-1f484d2c5738
ms.date: 12/05/2018
ms.keywords: ScrollPattern_SetScrollPercent, ScrollPattern_SetScrollPercent function [Windows Accessibility], uiauto.uiauto_ScrollPattern_SetScrollPercentConPat, uiauto_ScrollPattern_SetScrollPercentConPat, uiautomationcoreapi/ScrollPattern_SetScrollPercent, winauto.uiauto_ScrollPattern_SetScrollPercentConPat
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
 - ScrollPattern_SetScrollPercent
 - uiautomationcoreapi/ScrollPattern_SetScrollPercent
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
 - ScrollPattern_SetScrollPercent
---

# ScrollPattern_SetScrollPercent function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Scrolls a container to a specific position horizontally, vertically, or both.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.

### -param horizontalPercent [in]

Type: <b>double</b>

The horizontal position to scroll to.

### -param verticalPercent [in]

Type: <b>double</b>

The vertical position to scroll to.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The scroll area is normalized to range from 0.0 to 100.0. If the position is set to 0.0, the control 
scrolls to the beginning of the 
visible region, and if the position is set to 100.0, it  scrolls to the end of the visible region. 
Pass -1.0 for the percent parameters if no scrolling occurs on that axis.