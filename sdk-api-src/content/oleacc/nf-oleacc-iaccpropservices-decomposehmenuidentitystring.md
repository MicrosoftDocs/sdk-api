---
UID: NF:oleacc.IAccPropServices.DecomposeHmenuIdentityString
title: IAccPropServices::DecomposeHmenuIdentityString
author: windows-sdk-content
description: Use this method to determine the HMENU, object ID, and child ID for the accessible element identified by the identity string.
old-location: winauto\iaccpropservices_iaccpropservices__decomposehmenuidentitystring.htm
tech.root: WinAuto
ms.assetid: b76c4ba8-fb9a-438b-8547-b73b3c459ec6
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: DecomposeHmenuIdentityString, DecomposeHmenuIdentityString method [Windows Accessibility], DecomposeHmenuIdentityString method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],DecomposeHmenuIdentityString method, IAccPropServices.DecomposeHmenuIdentityString, IAccPropServices::DecomposeHmenuIdentityString, oleacc/IAccPropServices::DecomposeHmenuIdentityString, winauto.iaccpropservices_iaccpropservices__decomposehmenuidentitystring
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
 - IAccPropServices.DecomposeHmenuIdentityString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccPropServices::DecomposeHmenuIdentityString


## -description


Use this method to determine the <b>HMENU</b>, object ID, and child ID for the accessible element identified by the identity string.


## -parameters




### -param pIDString [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

Pointer to a buffer containing identity string of an <b>HMENU</b>-based accessible element.


### -param dwIDStringLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of the identity string specified by <i>pIDString</i>.


### -param phmenu [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a>*</b>

Pointer to a buffer that receives the <b>HMENU</b> of the accessible element.


### -param pidChild [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to a buffer that receives the child ID of the accessible element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if <i>phmenu</i> or <i>pidChild</i> are not valid, or if the given identity string is not a <b>HMENU</b>-based identity string.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



This method succeeds only if the provided identity string is an <b>HMENU</b>-based identity string. This method is useful in an <a href="https://msdn.microsoft.com/e82dfa58-9b36-4e42-9275-c09bad7bc730">IAccPropServer</a> callback server that was registered with ANNO_CONTAINER scope because it allows the server to determine, from the given identity string, the child element (<i>idChild</i>) for which the client is calling the server.



