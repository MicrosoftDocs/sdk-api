---
UID: NF:oleacc.IAccPropServices.ClearHwndProps
title: IAccPropServices::ClearHwndProps
author: windows-sdk-content
description: This method wraps SetPropValue, SetPropServer, and ClearProps, and provides a convenient entry point for callers who are annotating HWND-based accessible elements.
old-location: winauto\iaccpropservices_iaccpropservices__clearhwndprops.htm
old-project: WinAuto
ms.assetid: 7fd3f595-4897-481f-972e-04cf1a4c6046
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ClearHwndProps, ClearHwndProps method [Windows Accessibility], ClearHwndProps method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ClearHwndProps method, IAccPropServices.ClearHwndProps, IAccPropServices::ClearHwndProps, _msaa_IAccPropServices_ClearHwndProps, msaa.iaccpropservices_iaccpropservices__clearhwndprops, oleacc/IAccPropServices::ClearHwndProps, winauto.iaccpropservices_iaccpropservices__clearhwndprops
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
 - IAccPropServices.ClearHwndProps
product: Windows
targetos: Windows
req.lib: 
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
---

# IAccPropServices::ClearHwndProps


## -description


This method wraps <a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>, <a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>, and <a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a>, and provides a convenient entry point for callers who are annotating <b>HWND</b>-based accessible elements.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Identifies the accessible element that is to be annotated. This replaces the identity string.


### -param idObject [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Identifies the accessible element that is to be annotated. This replaces the identity string.


### -param idChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Identifies the accessible element that is to be annotated. This replaces the identity string.


### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specifies an array of properties that is to be reset. These properties will revert to the default behavior that they displayed before they were annotated.


### -param cProps [in]

Type: <b>int</b>

Specifies the number of properties in the <i>paProps</i> array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already-cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.

For descriptions of return values, see the corresponding <a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>, <a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>, or <a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a> method.




## -remarks



By using this method, the caller does not have to obtain an identity string; it can specify the <i>hwnd</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.

Additionally, <a href="https://msdn.microsoft.com/68f09a23-56b2-4fae-98a2-616b17fb4e1f">SetHwndPropStr</a> takes a regular Unicode string as a parameter; the caller does not need to specially allocate a <b>BSTR</b>.




## -see-also




<a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a>



<a href="https://msdn.microsoft.com/0474dacf-7aa1-4d12-bac2-1091676a1ced">IAccPropServices</a>



<a href="https://msdn.microsoft.com/00387897-5385-467d-9da4-4d71fce742b6">SetHwndProp</a>



<a href="https://msdn.microsoft.com/05dbdf97-9b1a-439f-b3a1-b517733ec0a8">SetHwndPropServer</a>



<a href="https://msdn.microsoft.com/68f09a23-56b2-4fae-98a2-616b17fb4e1f">SetHwndPropStr</a>
 

 

