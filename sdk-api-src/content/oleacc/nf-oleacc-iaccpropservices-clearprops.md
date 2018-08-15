---
UID: NF:oleacc.IAccPropServices.ClearProps
title: IAccPropServices::ClearProps
author: windows-sdk-content
description: Servers use ClearProps to restore default values to properties of accessible elements that they had previously annotated.
old-location: winauto\iaccpropservices_iaccpropservices__clearprops.htm
old-project: WinAuto
ms.assetid: 6a3bce93-1d5d-48cf-84f4-cbca445b5451
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClearProps, ClearProps method [Windows Accessibility], ClearProps method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ClearProps method, IAccPropServices.ClearProps, IAccPropServices::ClearProps, _msaa_IAccPropServices_ClearProps, msaa.iaccpropservices_iaccpropservices__clearprops, oleacc/IAccPropServices::ClearProps, winauto.iaccpropservices_iaccpropservices__clearprops
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
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
 - IAccPropServices.ClearProps
product: Windows
targetos: Windows
req.lib: 
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
---

# IAccPropServices::ClearProps


## -description


Servers use <b>ClearProps</b> to restore default values to properties of accessible elements that they had previously annotated.

If servers know the <b>HWND</b> of the object they want to clear, they can use <a href="https://msdn.microsoft.com/7fd3f595-4897-481f-972e-04cf1a4c6046">IAccPropServices::ClearHwndProps</a>.


## -parameters




### -param pIDString [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a>*</b>

Identify the accessible element that is to be un-annotated.


### -param dwIDStringLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Length of <i>pIDString</i>.


### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specify an array of properties that is to be reset. These properties will revert to the default behavior they displayed before they were annotated.


### -param cProps [in]

Type: <b>int</b>

Size of <i>paProps</i> array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.




## -remarks



See the support section for a list of supported properties and their expected types.

Clearing the annotation for a property will cause any associated resources to be released. If a callback property server was used (see <a href="https://msdn.microsoft.com/15e43a38-4cb3-43ca-a0fc-28faf49057dc">SetPropServer</a>), it will be released.



