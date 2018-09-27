---
UID: NF:oleacc.IAccPropServices.SetHwndPropServer
title: IAccPropServices::SetHwndPropServer
author: windows-sdk-content
description: This method wraps SetPropServer, providing a convenient entry point for callers who are annotating HWND-based accessible elements.
old-location: winauto\iaccpropservices_iaccpropservices__sethwndpropserver.htm
tech.root: WinAuto
ms.assetid: 05dbdf97-9b1a-439f-b3a1-b517733ec0a8
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHwndPropServer method, IAccPropServices.SetHwndPropServer, IAccPropServices::SetHwndPropServer, SetHwndPropServer, SetHwndPropServer method [Windows Accessibility], SetHwndPropServer method [Windows Accessibility],IAccPropServices interface, _msaa_IAccPropServices_SetHwndPropServer, msaa.iaccpropservices_iaccpropservices__sethwndpropserver, oleacc/IAccPropServices::SetHwndPropServer, winauto.iaccpropservices_iaccpropservices__sethwndpropserver
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
 - IAccPropServices.SetHwndPropServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccPropServices::SetHwndPropServer


## -description


This method wraps <a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>, providing a convenient entry point for callers who are annotating <b>HWND</b>-based accessible elements.


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

Specifies an array of properties that is to be handled by the specified callback object.


### -param cProps [in]

Type: <b>int</b>

Specifies the number of properties in the <i>paProps</i> array.


### -param pServer [in]

Type: <b>IAccPropServer*</b>

Specifies the callback object, which will be invoked when a client requests one of the overridden properties.


### -param annoScope [in]

Type: <b>AnnoScope</b>

May be ANNO_THIS, indicating that the annotation affects the indicated accessible element only; or ANNO_CONTAINER, indicating that it applies to the element and its immediate element children.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported properties, if the identity string is not valid, or if <i>annoScope</i> is not one of ANNO_THIS or ANNO_CONTAINER.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



By using this method, the caller does not have to obtain an identity string; it can specify the <i>hwnd</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.




## -see-also




<a href="https://msdn.microsoft.com/7fd3f595-4897-481f-972e-04cf1a4c6046">ClearHwndProps</a>



<a href="https://msdn.microsoft.com/0474dacf-7aa1-4d12-bac2-1091676a1ced">IAccPropServices</a>



<a href="https://msdn.microsoft.com/00387897-5385-467d-9da4-4d71fce742b6">SetHwndProp</a>



<a href="https://msdn.microsoft.com/68f09a23-56b2-4fae-98a2-616b17fb4e1f">SetHwndPropStr</a>



<a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>
 

 

