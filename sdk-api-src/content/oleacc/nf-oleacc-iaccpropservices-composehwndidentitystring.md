---
UID: NF:oleacc.IAccPropServices.ComposeHwndIdentityString
title: IAccPropServices::ComposeHwndIdentityString (oleacc.h)
description: Callers use ComposeHwndIdentityString to retrieve an identity string.
helpviewer_keywords: ["ComposeHwndIdentityString","ComposeHwndIdentityString method [Windows Accessibility]","ComposeHwndIdentityString method [Windows Accessibility]","IAccPropServices interface","IAccPropServices interface [Windows Accessibility]","ComposeHwndIdentityString method","IAccPropServices.ComposeHwndIdentityString","IAccPropServices::ComposeHwndIdentityString","_msaa_IAccPropServices_ComposeHwndIdentityString","msaa.iaccpropservices_iaccpropservices__composehwndidentitystring","oleacc/IAccPropServices::ComposeHwndIdentityString","winauto.iaccpropservices_iaccpropservices__composehwndidentitystring"]
old-location: winauto\iaccpropservices_iaccpropservices__composehwndidentitystring.htm
tech.root: WinAuto
ms.assetid: e6712e47-7f00-4932-9a12-40ecafdbf584
ms.date: 12/05/2018
ms.keywords: ComposeHwndIdentityString, ComposeHwndIdentityString method [Windows Accessibility], ComposeHwndIdentityString method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ComposeHwndIdentityString method, IAccPropServices.ComposeHwndIdentityString, IAccPropServices::ComposeHwndIdentityString, _msaa_IAccPropServices_ComposeHwndIdentityString, msaa.iaccpropservices_iaccpropservices__composehwndidentitystring, oleacc/IAccPropServices::ComposeHwndIdentityString, winauto.iaccpropservices_iaccpropservices__composehwndidentitystring
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
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
req.lib: 
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccPropServices::ComposeHwndIdentityString
 - oleacc/IAccPropServices::ComposeHwndIdentityString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServices.ComposeHwndIdentityString
---

# IAccPropServices::ComposeHwndIdentityString


## -description

Callers use <b>ComposeHwndIdentityString</b> 
		to retrieve an identity string.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Specifies the <b>HWND</b> of the accessible element that the caller wants to identify.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the object ID of the accessible element.

### -param idChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the child ID of the accessible element.

### -param ppIDString [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>**</b>

Pointer to a buffer that receives the identity string. The callee allocates this buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. When finished, the caller must free the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pdwIDStringLen [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer to a buffer that receives the length of the identity string.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if <i>hwnd</i>, <i>idObject</i>, or <i>idChild</i> is not valid.

May return other error codes under exceptional error conditions such as low memory.