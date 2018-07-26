---
UID: NF:oleacc.IAccPropServices.ComposeHwndIdentityString
title: IAccPropServices::ComposeHwndIdentityString
author: windows-sdk-content
description: Callers use ComposeHwndIdentityString to retrieve an identity string.
old-location: winauto\iaccpropservices_iaccpropservices__composehwndidentitystring.htm
old-project: WinAuto
ms.assetid: e6712e47-7f00-4932-9a12-40ecafdbf584
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ComposeHwndIdentityString, ComposeHwndIdentityString method [Windows Accessibility], ComposeHwndIdentityString method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ComposeHwndIdentityString method, IAccPropServices.ComposeHwndIdentityString, IAccPropServices::ComposeHwndIdentityString, _msaa_IAccPropServices_ComposeHwndIdentityString, msaa.iaccpropservices_iaccpropservices__composehwndidentitystring, oleacc/IAccPropServices::ComposeHwndIdentityString, winauto.iaccpropservices_iaccpropservices__composehwndidentitystring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServices.ComposeHwndIdentityString
product: Windows
targetos: Windows
req.lib: 
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
---

# IAccPropServices::ComposeHwndIdentityString


## -description


Callers use <b>ComposeHwndIdentityString</b> 
		to retrieve an identity string.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Specifies the <b>HWND</b> of the accessible element that the caller wants to identify.


### -param idObject [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the object ID of the accessible element.


### -param idChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the child ID of the accessible element.


### -param ppIDString [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>**</b>

Pointer to a buffer that receives the identity string. The callee allocates this buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. When finished, the caller must free the buffer by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pdwIDStringLen [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to a buffer that receives the length of the identity string.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if <i>hwnd</i>, <i>idObject</i>, or <i>idChild</i> is not valid.

May return other error codes under exceptional error conditions such as low memory.



