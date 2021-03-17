---
UID: NF:oleacc.IAccPropServices.ComposeHmenuIdentityString
title: IAccPropServices::ComposeHmenuIdentityString (oleacc.h)
description: Callers use ComposeHmenuIdentityString to retrieve an identity string for an HMENU-based accessible element.
helpviewer_keywords: ["ComposeHmenuIdentityString","ComposeHmenuIdentityString method [Windows Accessibility]","ComposeHmenuIdentityString method [Windows Accessibility]","IAccPropServices interface","IAccPropServices interface [Windows Accessibility]","ComposeHmenuIdentityString method","IAccPropServices.ComposeHmenuIdentityString","IAccPropServices::ComposeHmenuIdentityString","oleacc/IAccPropServices::ComposeHmenuIdentityString","winauto.iaccpropservices_iaccpropservices__composehmenuidentitystring"]
old-location: winauto\iaccpropservices_iaccpropservices__composehmenuidentitystring.htm
tech.root: WinAuto
ms.assetid: b0eb54e0-d903-46d8-a9f5-47f2c055c059
ms.date: 12/05/2018
ms.keywords: ComposeHmenuIdentityString, ComposeHmenuIdentityString method [Windows Accessibility], ComposeHmenuIdentityString method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ComposeHmenuIdentityString method, IAccPropServices.ComposeHmenuIdentityString, IAccPropServices::ComposeHmenuIdentityString, oleacc/IAccPropServices::ComposeHmenuIdentityString, winauto.iaccpropservices_iaccpropservices__composehmenuidentitystring
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
 - IAccPropServices::ComposeHmenuIdentityString
 - oleacc/IAccPropServices::ComposeHmenuIdentityString
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
 - IAccPropServices.ComposeHmenuIdentityString
---

# IAccPropServices::ComposeHmenuIdentityString


## -description

Callers use <b>ComposeHmenuIdentityString</b> 
		to retrieve an identity string for an <b>HMENU</b>-based accessible element.

## -parameters

### -param hmenu [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMENU</a></b>

Identifies the <b>HMENU</b>-based accessible element.

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

Returns E_INVALIDARG if <i>hmenu</i> or <i>idChild</i> is not valid.

May return other error codes under exceptional error conditions such as low memory.