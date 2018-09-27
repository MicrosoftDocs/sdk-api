---
UID: NF:oleacc.IAccPropServices.SetHmenuPropStr
title: IAccPropServices::SetHmenuPropStr
author: windows-sdk-content
description: This method wraps SetPropValue, providing a more convenient entry point for callers who are annotating HMENU-based accessible elements.
old-location: winauto\iaccpropservices_iaccpropservices__sethmenupropstr.htm
tech.root: WinAuto
ms.assetid: 891af40a-819b-4fce-a1bb-28db145b87f1
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHmenuPropStr method, IAccPropServices.SetHmenuPropStr, IAccPropServices::SetHmenuPropStr, SetHmenuPropStr, SetHmenuPropStr method [Windows Accessibility], SetHmenuPropStr method [Windows Accessibility],IAccPropServices interface, oleacc/IAccPropServices::SetHmenuPropStr, winauto.iaccpropservices_iaccpropservices__sethmenupropstr
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
 - IAccPropServices.SetHmenuPropStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccPropServices::SetHmenuPropStr


## -description


This method wraps <a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>, providing a more convenient entry point for callers who are annotating <b>HMENU</b>-based accessible elements.


## -parameters




### -param hmenu [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a></b>

Identifies the <b>HMENU</b>-based accessible element to be annotated.


### -param idChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the child ID of the accessible element.


### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies which property of the accessible element is to be annotated.


### -param str [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

Specifies a new value for the <i>idProp</i> property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



By using this method, the caller does not have to obtain an identity string; it can specify the <i>hmenu</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.




## -see-also




<a href="https://msdn.microsoft.com/dbff74b0-c67b-4ef4-add7-6063c4760455">ClearHmenuProps</a>



<a href="https://msdn.microsoft.com/0474dacf-7aa1-4d12-bac2-1091676a1ced">IAccPropServices</a>



<a href="https://msdn.microsoft.com/ac835bb6-609f-4a37-8cfc-dd529d641c00">SetHmenuProp</a>



<a href="https://msdn.microsoft.com/7bc91ee3-f0ea-43d5-a8b7-d1444c53cd14">SetHmenuPropServer</a>



<a href="https://msdn.microsoft.com/c86acb70-fa77-4f95-8a99-e60872cdaa7e">SetPropValue</a>
 

 

