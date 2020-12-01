---
UID: NF:uiautomationcoreapi.UiaHUiaNodeFromVariant
title: UiaHUiaNodeFromVariant function (uiautomationcoreapi.h)
description: Gets an HUIANODE from a VARIANT type.
helpviewer_keywords: ["UiaHUiaNodeFromVariant","UiaHUiaNodeFromVariant function [Windows Accessibility]","uiauto.uiauto_UiaHUiaNodeFromVariantFunction","uiauto_UiaHUiaNodeFromVariantFunction","uiautomationcoreapi/UiaHUiaNodeFromVariant","winauto.uiauto_UiaHUiaNodeFromVariantFunction"]
old-location: winauto\uiauto_UiaHUiaNodeFromVariantFunction.htm
tech.root: WinAuto
ms.assetid: 9927a058-a470-4b0e-86ae-494a8ab0ec2c
ms.date: 12/05/2018
ms.keywords: UiaHUiaNodeFromVariant, UiaHUiaNodeFromVariant function [Windows Accessibility], uiauto.uiauto_UiaHUiaNodeFromVariantFunction, uiauto_UiaHUiaNodeFromVariantFunction, uiautomationcoreapi/UiaHUiaNodeFromVariant, winauto.uiauto_UiaHUiaNodeFromVariantFunction
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
 - UiaHUiaNodeFromVariant
 - uiautomationcoreapi/UiaHUiaNodeFromVariant
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
 - UiaHUiaNodeFromVariant
---

# UiaHUiaNodeFromVariant function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Gets an HUIANODE from a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> type.

## -parameters

### -param pvar [in]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

The node.

### -param phnode [out]

Type: <b>HUIANODE*</b>

The address of a variable that receives the HUIANODE.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.