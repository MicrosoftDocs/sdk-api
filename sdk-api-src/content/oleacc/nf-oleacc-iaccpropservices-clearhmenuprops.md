---
UID: NF:oleacc.IAccPropServices.ClearHmenuProps
title: IAccPropServices::ClearHmenuProps
author: windows-driver-content
description: This method wraps ClearProps, and provides a convenient entry point for callers who are annotating HMENU-based accessible elements.
old-location: winauto\iaccpropservices_iaccpropservices__clearhmenuprops.htm
old-project: WinAuto
ms.assetid: dbff74b0-c67b-4ef4-add7-6063c4760455
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ClearHmenuProps, ClearHmenuProps method [Windows Accessibility], ClearHmenuProps method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ClearHmenuProps method, IAccPropServices.ClearHmenuProps, IAccPropServices::ClearHmenuProps, oleacc/IAccPropServices::ClearHmenuProps, winauto.iaccpropservices_iaccpropservices__clearhmenuprops
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Oleacc.dll
api_name:
-	IAccPropServices.ClearHmenuProps
product: Windows
targetos: Windows
req.lib: 
req.dll: Oleacc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAccPropServices::ClearHmenuProps


## -description


This method wraps  <a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a>, and provides a convenient entry point for callers who are annotating <b>HMENU</b>-based accessible elements.


## -parameters




### -param hmenu [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HMENU</a></b>

Identifies the <b>HMENU</b>-based accessible element to be annotated.


### -param idChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the child ID of the accessible element.


### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specifies an array of properties to be reset. These properties will revert to the default behavior that they displayed before they were annotated.


### -param cProps [in]

Type: <b>int</b>

Specifies the number of properties in the <i>paProps</i> array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already-cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.

For descriptions of other parameters and return values, see the <a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a> method.




## -remarks



By using this method, the caller does not have to obtain an identity string; it can specify the <i>hmenu</i> and <i>idChild</i> parameters directly.




## -see-also




<a href="https://msdn.microsoft.com/6a3bce93-1d5d-48cf-84f4-cbca445b5451">ClearProps</a>



<a href="https://msdn.microsoft.com/0474dacf-7aa1-4d12-bac2-1091676a1ced">IAccPropServices</a>



<a href="https://msdn.microsoft.com/ac835bb6-609f-4a37-8cfc-dd529d641c00">SetHmenuProp</a>



<a href="https://msdn.microsoft.com/7bc91ee3-f0ea-43d5-a8b7-d1444c53cd14">SetHmenuPropServer</a>



<a href="https://msdn.microsoft.com/891af40a-819b-4fce-a1bb-28db145b87f1">SetHmenuPropStr</a>
 

 

