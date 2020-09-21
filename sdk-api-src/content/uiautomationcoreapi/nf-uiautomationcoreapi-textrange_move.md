---
UID: NF:uiautomationcoreapi.TextRange_Move
title: TextRange_Move function (uiautomationcoreapi.h)
description: Moves the text range the specified number of units requested by the client.
helpviewer_keywords: ["TextRange_Move","TextRange_Move function [Windows Accessibility]","uiauto.uiauto_TextRange_MoveConPat","uiauto_TextRange_MoveConPat","uiautomationcoreapi/TextRange_Move","winauto.uiauto_TextRange_MoveConPat"]
old-location: winauto\uiauto_TextRange_MoveConPat.htm
tech.root: WinAuto
ms.assetid: 9d63bd12-da79-46b4-ad93-cd940948a0f5
ms.date: 12/05/2018
ms.keywords: TextRange_Move, TextRange_Move function [Windows Accessibility], uiauto.uiauto_TextRange_MoveConPat, uiauto_TextRange_MoveConPat, uiautomationcoreapi/TextRange_Move, winauto.uiauto_TextRange_MoveConPat
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
 - TextRange_Move
 - uiautomationcoreapi/TextRange_Move
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
 - TextRange_Move
---

# TextRange_Move function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Moves the text range the specified number of units requested by the client.

## -parameters

### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

A text range object.

### -param unit [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-textunit">TextUnit</a></b>

The unit, such as Page, Line, or Word.

### -param count [in]

Type: <b>int</b>

The number of units to move. Positive numbers move the range forward, 
				and negative numbers move the range backward.

### -param pRetVal [out]

Type: <b>int*</b>

When this function returns, contains 
				the number of units actually moved.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.