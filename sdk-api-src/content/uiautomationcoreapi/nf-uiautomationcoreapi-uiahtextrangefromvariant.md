---
UID: NF:uiautomationcoreapi.UiaHTextRangeFromVariant
title: UiaHTextRangeFromVariant function (uiautomationcoreapi.h)
description: Gets a text range from a VARIANT type.
helpviewer_keywords: ["UiaHTextRangeFromVariant","UiaHTextRangeFromVariant function [Windows Accessibility]","uiauto.uiauto_UiaHTextRangeFromVariantFunction","uiauto_UiaHTextRangeFromVariantFunction","uiautomationcoreapi/UiaHTextRangeFromVariant","winauto.uiauto_UiaHTextRangeFromVariantFunction"]
old-location: winauto\uiauto_UiaHTextRangeFromVariantFunction.htm
tech.root: WinAuto
ms.assetid: 139b970f-614c-42ff-b1d1-4d8644d98d06
ms.date: 12/05/2018
ms.keywords: UiaHTextRangeFromVariant, UiaHTextRangeFromVariant function [Windows Accessibility], uiauto.uiauto_UiaHTextRangeFromVariantFunction, uiauto_UiaHTextRangeFromVariantFunction, uiautomationcoreapi/UiaHTextRangeFromVariant, winauto.uiauto_UiaHTextRangeFromVariantFunction
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
 - UiaHTextRangeFromVariant
 - uiautomationcoreapi/UiaHTextRangeFromVariant
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
 - UiaHTextRangeFromVariant
---

# UiaHTextRangeFromVariant function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets a text range from a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> type.

## -parameters

### -param pvar [in]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

The text range.

### -param phtextrange [out]

Type: <b>HUIATEXTRANGE*</b>

The address of a variable that receives the text range.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.