---
UID: NF:uiautomationcoreapi.TextRange_CompareEndpoints
title: TextRange_CompareEndpoints function (uiautomationcoreapi.h)
description: Returns a value indicating whether two text ranges have identical endpoints.
helpviewer_keywords: ["TextRange_CompareEndpoints","TextRange_CompareEndpoints function [Windows Accessibility]","uiauto.uiauto_TextRange_CompareEndpointsConPat","uiauto_TextRange_CompareEndpointsConPat","uiautomationcoreapi/TextRange_CompareEndpoints","winauto.uiauto_TextRange_CompareEndpointsConPat"]
old-location: winauto\uiauto_TextRange_CompareEndpointsConPat.htm
tech.root: WinAuto
ms.assetid: f396ec3e-f491-48be-8282-42c3b8698f3a
ms.date: 12/05/2018
ms.keywords: TextRange_CompareEndpoints, TextRange_CompareEndpoints function [Windows Accessibility], uiauto.uiauto_TextRange_CompareEndpointsConPat, uiauto_TextRange_CompareEndpointsConPat, uiautomationcoreapi/TextRange_CompareEndpoints, winauto.uiauto_TextRange_CompareEndpointsConPat
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
 - TextRange_CompareEndpoints
 - uiautomationcoreapi/TextRange_CompareEndpoints
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
 - TextRange_CompareEndpoints
---

# TextRange_CompareEndpoints function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Returns a value indicating whether two text ranges have identical endpoints.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The starting or ending endpoint of <i>hobj</i>.

### -param targetRange [in]

Type: <b>ITextRangeInteropProvider*</b>

The text range that is being compared against.

### -param targetEndpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The starting or ending endpoint of <i>targetRange</i>.

### -param pRetVal [out]

Type: <b>int*</b>

The address of a variable that receives a pointer to a value that indicates whether two text ranges have identical endpoints.
				 This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

The returned value is &lt;0 if the caller's endpoint occurs earlier in the text than the target endpoint; 
			0 if the caller's endpoint is at the same location as the target endpoint; and 
			&gt;0 if the caller's endpoint occurs later in the text than the target endpoint.