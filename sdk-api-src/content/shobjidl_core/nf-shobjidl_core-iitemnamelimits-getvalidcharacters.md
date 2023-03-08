---
UID: NF:shobjidl_core.IItemNameLimits.GetValidCharacters
title: IItemNameLimits::GetValidCharacters (shobjidl_core.h)
description: Loads a string that contains each of the characters that are valid or invalid in the namespace under which it is called.
helpviewer_keywords: ["GetValidCharacters","GetValidCharacters method [Windows Shell]","GetValidCharacters method [Windows Shell]","IItemNameLimits interface","IItemNameLimits interface [Windows Shell]","GetValidCharacters method","IItemNameLimits.GetValidCharacters","IItemNameLimits::GetValidCharacters","_shell_IItemNameLimits_GetValidCharacters","shell.IItemNameLimits_GetValidCharacters","shobjidl_core/IItemNameLimits::GetValidCharacters"]
old-location: shell\IItemNameLimits_GetValidCharacters.htm
tech.root: shell
ms.assetid: a6328be9-accd-4f11-82ee-49d3b18f9fd6
ms.date: 12/05/2018
ms.keywords: GetValidCharacters, GetValidCharacters method [Windows Shell], GetValidCharacters method [Windows Shell],IItemNameLimits interface, IItemNameLimits interface [Windows Shell],GetValidCharacters method, IItemNameLimits.GetValidCharacters, IItemNameLimits::GetValidCharacters, _shell_IItemNameLimits_GetValidCharacters, shell.IItemNameLimits_GetValidCharacters, shobjidl_core/IItemNameLimits::GetValidCharacters
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IItemNameLimits::GetValidCharacters
 - shobjidl_core/IItemNameLimits::GetValidCharacters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IItemNameLimits.GetValidCharacters
---

# IItemNameLimits::GetValidCharacters


## -description

Loads a string that contains each of the characters that are valid or invalid in the namespace under which it is called.

## -parameters

### -param ppwszValidChars [out]

Type: <b>LPWSTR*</b>

A pointer to a string that contains all valid characters in the namespace. If the namespace provides <i>any</i> invalid characters in <i>ppwszInvalidChars</i>, then this value returns <b>NULL</b>. See Remarks for more details.

### -param ppwszInvalidChars [out]

Type: <b>LPWSTR*</b>

A pointer to a string that contains all invalid characters in the namespace.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

As an example, the standard file system returns the string "\/:*?"&lt;&gt;|" in <i>ppwszInvalidChars</i> and <b>NULL</b> in <i>ppwszValidChars</i>. 

Both parameters cannot return non-<b>NULL</b> values, so <i>ppwszValidChars</i> is assigned a value of <b>NULL</b> because of the non-<b>NULL</b> value 

in <i>ppwszInvalidChars</i>. It is assumed that when there are specified invalid characters, everything else is valid. Only when <i>ppwszInvalidChars</i> is <b>NULL</b> does <i>ppwszValidChars</i> contain a list of all valid characters.
			

If the method returns a success code, the allocated string must be freed using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.