---
UID: NF:uiautomationcoreapi.UiaPatternRelease
title: UiaPatternRelease function (uiautomationcoreapi.h)
description: Deletes an allocated pattern object from memory.
helpviewer_keywords: ["UiaPatternRelease","UiaPatternRelease function [Windows Accessibility]","uiauto.uiauto_UiaPatternReleaseMemManMeth","uiauto_UiaPatternReleaseMemManMeth","uiautomationcoreapi/UiaPatternRelease","winauto.uiauto_UiaPatternReleaseMemManMeth"]
old-location: winauto\uiauto_UiaPatternReleaseMemManMeth.htm
tech.root: WinAuto
ms.assetid: caa7231b-5b31-499e-b548-479501ddf016
ms.date: 12/05/2018
ms.keywords: UiaPatternRelease, UiaPatternRelease function [Windows Accessibility], uiauto.uiauto_UiaPatternReleaseMemManMeth, uiauto_UiaPatternReleaseMemManMeth, uiautomationcoreapi/UiaPatternRelease, winauto.uiauto_UiaPatternReleaseMemManMeth
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
 - UiaPatternRelease
 - uiautomationcoreapi/UiaPatternRelease
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
 - UiaPatternRelease
---

# UiaPatternRelease function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Deletes an allocated pattern object from memory.

## -parameters

### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The pattern object to be deleted.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the pattern was successfully deleted; otherwise <b>FALSE</b>.