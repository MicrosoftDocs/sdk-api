---
UID: NF:uiautomationcoreapi.TextRange_AddToSelection
title: TextRange_AddToSelection function (uiautomationcoreapi.h)
description: Adds to the existing collection of highlighted text in a text container that supports multiple, disjoint selections by highlighting supplementary text corresponding to the calling text range Start and End endpoints.
helpviewer_keywords: ["TextRange_AddToSelection","TextRange_AddToSelection function [Windows Accessibility]","uiauto.uiauto_TextRange_AddToSelectionConPat","uiauto_TextRange_AddToSelectionConPat","uiautomationcoreapi/TextRange_AddToSelection","winauto.uiauto_TextRange_AddToSelectionConPat"]
old-location: winauto\uiauto_TextRange_AddToSelectionConPat.htm
tech.root: WinAuto
ms.assetid: a9e832ea-5761-4c5d-839e-9d4db2c551c2
ms.date: 12/05/2018
ms.keywords: TextRange_AddToSelection, TextRange_AddToSelection function [Windows Accessibility], uiauto.uiauto_TextRange_AddToSelectionConPat, uiauto_TextRange_AddToSelectionConPat, uiautomationcoreapi/TextRange_AddToSelection, winauto.uiauto_TextRange_AddToSelectionConPat
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
 - TextRange_AddToSelection
 - uiautomationcoreapi/TextRange_AddToSelection
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
 - TextRange_AddToSelection
---

# TextRange_AddToSelection function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Adds to the existing collection of highlighted text in a text container 
        that supports multiple, disjoint selections by highlighting supplementary text 
        corresponding to the calling text range <i>Start</i> 
        and <i>End</i> endpoints.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.