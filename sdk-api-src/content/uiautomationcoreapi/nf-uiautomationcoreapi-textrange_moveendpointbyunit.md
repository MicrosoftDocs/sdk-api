---
UID: NF:uiautomationcoreapi.TextRange_MoveEndpointByUnit
title: TextRange_MoveEndpointByUnit function (uiautomationcoreapi.h)
description: Moves an endpoint of the range the specified number of units.
helpviewer_keywords: ["TextRange_MoveEndpointByUnit","TextRange_MoveEndpointByUnit function [Windows Accessibility]","uiauto.uiauto_TextRange_MoveEndpointByUnitConPat","uiauto_TextRange_MoveEndpointByUnitConPat","uiautomationcoreapi/TextRange_MoveEndpointByUnit","winauto.uiauto_TextRange_MoveEndpointByUnitConPat"]
old-location: winauto\uiauto_TextRange_MoveEndpointByUnitConPat.htm
tech.root: WinAuto
ms.assetid: 15afd438-c662-4cc1-b6b5-87e5bf82ccaa
ms.date: 12/05/2018
ms.keywords: TextRange_MoveEndpointByUnit, TextRange_MoveEndpointByUnit function [Windows Accessibility], uiauto.uiauto_TextRange_MoveEndpointByUnitConPat, uiauto_TextRange_MoveEndpointByUnitConPat, uiautomationcoreapi/TextRange_MoveEndpointByUnit, winauto.uiauto_TextRange_MoveEndpointByUnitConPat
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
 - TextRange_MoveEndpointByUnit
 - uiautomationcoreapi/TextRange_MoveEndpointByUnit
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
 - TextRange_MoveEndpointByUnit
---

# TextRange_MoveEndpointByUnit function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Moves an endpoint of the range the specified number of units.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The endpoint to move (either the start or the end).

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The unit, such as Page, Line, or Word.

### -param count [in]

Type: <b>int</b>

The number of units to move. A positive value moves the range forward; a negative value
				moves it backward.

### -param pRetVal [out]

Type: <b>int*</b>

When this function returns, contains 
				the number of units the endpoint actually moved.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.