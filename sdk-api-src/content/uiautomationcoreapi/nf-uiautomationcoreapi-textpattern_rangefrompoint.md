---
UID: NF:uiautomationcoreapi.TextPattern_RangeFromPoint
title: TextPattern_RangeFromPoint function (uiautomationcoreapi.h)
description: Retrieves the degenerate (empty) text range nearest to the specified screen coordinates. (TextPattern_RangeFromPoint)
helpviewer_keywords: ["TextPattern_RangeFromPoint","TextPattern_RangeFromPoint function [Windows Accessibility]","uiauto.uiauto_TextPattern_RangeFromPointConPat","uiauto_TextPattern_RangeFromPointConPat","uiautomationcoreapi/TextPattern_RangeFromPoint","winauto.uiauto_TextPattern_RangeFromPointConPat"]
old-location: winauto\uiauto_TextPattern_RangeFromPointConPat.htm
tech.root: WinAuto
ms.assetid: 242c69fd-4d01-4671-9794-c8ee3e4def8f
ms.date: 12/05/2018
ms.keywords: TextPattern_RangeFromPoint, TextPattern_RangeFromPoint function [Windows Accessibility], uiauto.uiauto_TextPattern_RangeFromPointConPat, uiauto_TextPattern_RangeFromPointConPat, uiautomationcoreapi/TextPattern_RangeFromPoint, winauto.uiauto_TextPattern_RangeFromPointConPat
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
 - TextPattern_RangeFromPoint
 - uiautomationcoreapi/TextPattern_RangeFromPoint
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
 - TextPattern_RangeFromPoint
---

# TextPattern_RangeFromPoint function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.

### -param point [in]

Type: <b>HiaPoint</b>

A <a href="/windows/desktop/api/uiautomationcore/ns-uiautomationcore-uiapoint">UiaPoint</a> structure that contains the location in screen coordinates.

### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains the text range that the node spans. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

A text range that wraps a child object is returned if the screen coordinates are within the coordinates of an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.

Because hidden text is not ignored, this method retrieves a degenerate range from the visible text closest to the specified coordinates.
