---
UID: NF:uiautomationcoreapi.UiaTextRangeRelease
title: UiaTextRangeRelease function (uiautomationcoreapi.h)
description: Deletes an allocated text range object from memory.helpviewer_keywords: ["UiaTextRangeRelease","UiaTextRangeRelease function [Windows Accessibility]","uiauto.uiauto_UiaTextRangeReleaseMemManMeth","uiauto_UiaTextRangeReleaseMemManMeth","uiautomationcoreapi/UiaTextRangeRelease","winauto.uiauto_UiaTextRangeReleaseMemManMeth"]
old-location: winauto\uiauto_UiaTextRangeReleaseMemManMeth.htm
tech.root: WinAuto
ms.assetid: 20607071-6300-47f9-8d12-5cf8cc51072a
ms.date: 12/05/2018
ms.keywords: UiaTextRangeRelease, UiaTextRangeRelease function [Windows Accessibility], uiauto.uiauto_UiaTextRangeReleaseMemManMeth, uiauto_UiaTextRangeReleaseMemManMeth, uiautomationcoreapi/UiaTextRangeRelease, winauto.uiauto_UiaTextRangeReleaseMemManMeth
f1_keywords:
- uiautomationcoreapi/UiaTextRangeRelease
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Uiautomationcore.dll
api_name:
- UiaTextRangeRelease
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UiaTextRangeRelease function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Deletes an allocated text range object from memory.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range object to be deleted.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if object was deleted; otherwise <b>FALSE</b>.



