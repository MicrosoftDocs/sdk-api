---
UID: NF:oleacc.IAccIdentity.GetIdentityString
title: IAccIdentity::GetIdentityString
author: windows-sdk-content
description: Retrieves a string of bytes (an identity string) that uniquely identifies an accessible element.
old-location: winauto\iaccidentity_iaccidentity__getidentitystring.htm
tech.root: WinAuto
ms.assetid: 38467491-c432-456a-9128-723fc7dde189
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetIdentityString, GetIdentityString method [Windows Accessibility], GetIdentityString method [Windows Accessibility],IAccIdentity interface, IAccIdentity interface [Windows Accessibility],GetIdentityString method, IAccIdentity.GetIdentityString, IAccIdentity::GetIdentityString, _msaa_IAccIdentity_GetIdentityString, msaa.iaccidentity_iaccidentity__getidentitystring, oleacc/IAccIdentity::GetIdentityString, winauto.iaccidentity_iaccidentity__getidentitystring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.target-type: Windows
req.target-min-winverclnt: Windows Vista or Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - IAccIdentity.GetIdentityString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccIdentity::GetIdentityString


## -description


Retrieves a string of bytes (an identity string) that uniquely identifies an accessible element.

If server developers know the <b>HWND</b> of the object they want to annotate, they can use one of the following methods instead of using this 
		method and getting an identity string.
<ul>
<li>
<a href="https://msdn.microsoft.com/68f09a23-56b2-4fae-98a2-616b17fb4e1f">IAccPropServices::SetHwndPropStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/00387897-5385-467d-9da4-4d71fce742b6">IAccPropServices::SetHwndProp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/05dbdf97-9b1a-439f-b3a1-b517733ec0a8">IAccPropServices::SetHwndPropServer</a>
</li>
</ul>

## -parameters




### -param dwIDChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies which child of the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object the caller wants to identify.


### -param ppIDString [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>**</b>

Address of a variable that receives a pointer to a callee-allocated identity string. The callee allocates the identity string using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>; the caller must release the identity string by using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when finished.


### -param pdwIDStringLen [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Address of a variable that receives the length, in bytes, of the callee-allocated identity string.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK, except under exceptional error conditions, such as low memory. If not supported, calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on <a href="https://msdn.microsoft.com/59fde1a5-42bd-40e0-8143-edd082b2b166">IAccIdentity</a> should fail.




## -remarks



The returned string should be considered opaque; clients should use it only as a whole, and should not attempt to dissect it or otherwise interpret it manually.

If a client knows or expects that a string is HWND—based, it can use <a href="https://msdn.microsoft.com/b14932a1-7585-49e4-80eb-498cf48796ee">IAccPropServices::DecomposeHwndIdentityString</a> to attempt to decompose the identity string.



