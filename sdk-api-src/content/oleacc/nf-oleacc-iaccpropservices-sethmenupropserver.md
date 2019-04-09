---
UID: NF:oleacc.IAccPropServices.SetHmenuPropServer
title: IAccPropServices::SetHmenuPropServer (oleacc.h)
author: windows-sdk-content
description: This method wraps SetPropServer, providing a convenient entry point for callers who are annotating HMENU-based accessible elements.
old-location: winauto\iaccpropservices_iaccpropservices__sethmenupropserver.htm
tech.root: WinAuto
ms.assetid: 7bc91ee3-f0ea-43d5-a8b7-d1444c53cd14
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHmenuPropServer method, IAccPropServices.SetHmenuPropServer, IAccPropServices::SetHmenuPropServer, SetHmenuPropServer, SetHmenuPropServer method [Windows Accessibility], SetHmenuPropServer method [Windows Accessibility],IAccPropServices interface, oleacc/IAccPropServices::SetHmenuPropServer, winauto.iaccpropservices_iaccpropservices__sethmenupropserver
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
 - IAccPropServices.SetHmenuPropServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccPropServices::SetHmenuPropServer


## -description


This method wraps <a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>, providing a convenient entry point for callers who are annotating <b>HMENU</b>-based accessible elements.


## -parameters




### -param hmenu [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a></b>

Identifies the <b>HMENU</b>-accessible element to be annotated.


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



By using this method, the caller does not have to obtain an identity string; it can specify the <i>hmenu</i> and <i>idChild</i> parameters directly.




## -see-also




<a href="https://msdn.microsoft.com/dbff74b0-c67b-4ef4-add7-6063c4760455">ClearHmenuProps</a>



<a href="https://msdn.microsoft.com/0474dacf-7aa1-4d12-bac2-1091676a1ced">IAccPropServices</a>



<a href="https://msdn.microsoft.com/ac835bb6-609f-4a37-8cfc-dd529d641c00">SetHmenuProp</a>



<a href="https://msdn.microsoft.com/891af40a-819b-4fce-a1bb-28db145b87f1">SetHmenuPropStr</a>



<a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>
 

 

