---
UID: NF:uiautomationcoreapi.TextPattern_RangeFromChild
title: TextPattern_RangeFromChild function (uiautomationcoreapi.h)
description: Gets the text range that a given node spans.
helpviewer_keywords: ["TextPattern_RangeFromChild","TextPattern_RangeFromChild function [Windows Accessibility]","uiauto.uiauto_TextPattern_RangeFromChildConPat","uiauto_TextPattern_RangeFromChildConPat","uiautomationcoreapi/TextPattern_RangeFromChild","winauto.uiauto_TextPattern_RangeFromChildConPat"]
old-location: winauto\uiauto_TextPattern_RangeFromChildConPat.htm
tech.root: WinAuto
ms.assetid: 9745b837-f185-48c5-94d6-30c93fa58313
ms.date: 12/05/2018
ms.keywords: TextPattern_RangeFromChild, TextPattern_RangeFromChild function [Windows Accessibility], uiauto.uiauto_TextPattern_RangeFromChildConPat, uiauto_TextPattern_RangeFromChildConPat, uiautomationcoreapi/TextPattern_RangeFromChild, winauto.uiauto_TextPattern_RangeFromChildConPat
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
 - TextPattern_RangeFromChild
 - uiautomationcoreapi/TextPattern_RangeFromChild
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
 - TextPattern_RangeFromChild
---

# TextPattern_RangeFromChild function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets the text range that a given node spans.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.

### -param hnodeChild [in]

Type: <b>HUIANODE</b>

Reference to a node that the client wants the text range for.

### -param pRetVal [out]

Type: <b>HUIATEXTRANGE*</b>

When this function returns, contains the text range that the node spans. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -remarks

As an example of how this function might be used, 
a client can pass in an embedded hyperlink control and receive the range of text that it spans.