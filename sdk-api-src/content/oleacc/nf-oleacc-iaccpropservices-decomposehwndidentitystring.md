---
UID: NF:oleacc.IAccPropServices.DecomposeHwndIdentityString
title: IAccPropServices::DecomposeHwndIdentityString
author: windows-sdk-content
description: Use this method to determine the HWND, object ID, and child ID for the accessible element identified by the identity string.
old-location: winauto\iaccpropservices_iaccpropservices__decomposehwndidentitystring.htm
tech.root: WinAuto
ms.assetid: b14932a1-7585-49e4-80eb-498cf48796ee
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DecomposeHwndIdentityString, DecomposeHwndIdentityString method [Windows Accessibility], DecomposeHwndIdentityString method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],DecomposeHwndIdentityString method, IAccPropServices.DecomposeHwndIdentityString, IAccPropServices::DecomposeHwndIdentityString, _msaa_IAccPropServices_DecomposeHwndIdentityString, msaa.iaccpropservices_iaccpropservices__decomposehwndidentitystring, oleacc/IAccPropServices::DecomposeHwndIdentityString, winauto.iaccpropservices_iaccpropservices__decomposehwndidentitystring
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServices.DecomposeHwndIdentityString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccPropServices::DecomposeHwndIdentityString


## -description


Use this method to determine the <b>HWND</b>, object ID, and child ID for the accessible element identified by the identity string.


## -parameters




### -param pIDString [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

Pointer to a buffer containing identity string of an <b>HWND</b>-based accessible element.


### -param dwIDStringLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of the identity string specified by <i>pIDString</i>.


### -param phwnd [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>*</b>

Pointer to a buffer that receives the <b>HWND</b> of the accessible element.


### -param pidObject [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to a buffer that receives the object ID of the accessible element.


### -param pidChild [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to a buffer that receives the child ID of the accessible element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if <i>phwnd</i>, <i>pidObject</i>, or <i>pidChild</i> are not valid, or if the given identity string is not a <b>HWND</b>-based identity string.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



This method succeeds only if the provided identity string is a <b>HWND</b>-based identity string. This method is useful when used in an <a href="https://msdn.microsoft.com/e82dfa58-9b36-4e42-9275-c09bad7bc730">IAccPropServer</a> callback server that was registered with ANNO_CONTAINER scope because it allows the server to determine, from the given identity string, the child element (<i>idChild</i>) for which the client is calling the server.



