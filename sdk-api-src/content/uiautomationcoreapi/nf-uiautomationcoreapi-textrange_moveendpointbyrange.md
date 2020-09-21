---
UID: NF:uiautomationcoreapi.TextRange_MoveEndpointByRange
title: TextRange_MoveEndpointByRange function (uiautomationcoreapi.h)
description: Moves an endpoint of one range to the endpoint of another range.
helpviewer_keywords: ["TextRange_MoveEndpointByRange","TextRange_MoveEndpointByRange function [Windows Accessibility]","uiauto.uiauto_TextRange_MoveEndpointByRangeConPat","uiauto_TextRange_MoveEndpointByRangeConPat","uiautomationcoreapi/TextRange_MoveEndpointByRange","winauto.uiauto_TextRange_MoveEndpointByRangeConPat"]
old-location: winauto\uiauto_TextRange_MoveEndpointByRangeConPat.htm
tech.root: WinAuto
ms.assetid: ec26280d-76f2-447b-9547-0484c5140e89
ms.date: 12/05/2018
ms.keywords: TextRange_MoveEndpointByRange, TextRange_MoveEndpointByRange function [Windows Accessibility], uiauto.uiauto_TextRange_MoveEndpointByRangeConPat, uiauto_TextRange_MoveEndpointByRangeConPat, uiautomationcoreapi/TextRange_MoveEndpointByRange, winauto.uiauto_TextRange_MoveEndpointByRangeConPat
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
 - TextRange_MoveEndpointByRange
 - uiautomationcoreapi/TextRange_MoveEndpointByRange
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
 - TextRange_MoveEndpointByRange
---

# TextRange_MoveEndpointByRange function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Moves an endpoint of one range to the endpoint of another range.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range object whose endpoint is to move.

### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The endpoint to move (either the start or the end).

### -param targetRange [in]

Type: <b>HUIATEXTRANGE</b>

The text range that contains the target endpoint.

### -param targetEndpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The target endpoint to move to (either the start or the end).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.