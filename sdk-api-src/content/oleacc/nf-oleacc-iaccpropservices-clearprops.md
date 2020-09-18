---
UID: NF:oleacc.IAccPropServices.ClearProps
title: IAccPropServices::ClearProps (oleacc.h)
description: Servers use ClearProps to restore default values to properties of accessible elements that they had previously annotated.
helpviewer_keywords: ["ClearProps","ClearProps method [Windows Accessibility]","ClearProps method [Windows Accessibility]","IAccPropServices interface","IAccPropServices interface [Windows Accessibility]","ClearProps method","IAccPropServices.ClearProps","IAccPropServices::ClearProps","_msaa_IAccPropServices_ClearProps","msaa.iaccpropservices_iaccpropservices__clearprops","oleacc/IAccPropServices::ClearProps","winauto.iaccpropservices_iaccpropservices__clearprops"]
old-location: winauto\iaccpropservices_iaccpropservices__clearprops.htm
tech.root: WinAuto
ms.assetid: 6a3bce93-1d5d-48cf-84f4-cbca445b5451
ms.date: 12/05/2018
ms.keywords: ClearProps, ClearProps method [Windows Accessibility], ClearProps method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ClearProps method, IAccPropServices.ClearProps, IAccPropServices::ClearProps, _msaa_IAccPropServices_ClearProps, msaa.iaccpropservices_iaccpropservices__clearprops, oleacc/IAccPropServices::ClearProps, winauto.iaccpropservices_iaccpropservices__clearprops
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
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IAccPropServices::ClearProps
 - oleacc/IAccPropServices::ClearProps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServices.ClearProps
---

# IAccPropServices::ClearProps


## -description

Servers use <b>ClearProps</b> to restore default values to properties of accessible elements that they had previously annotated.

If servers know the <b>HWND</b> of the object they want to clear, they can use <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearhwndprops">IAccPropServices::ClearHwndProps</a>.

## -parameters

### -param pIDString [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>*</b>

Identify the accessible element that is to be un-annotated.

### -param dwIDStringLen [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Length of <i>pIDString</i>.

### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specify an array of properties that is to be reset. These properties will revert to the default behavior they displayed before they were annotated.

### -param cProps [in]

Type: <b>int</b>

Size of <i>paProps</i> array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

See the support section for a list of supported properties and their expected types.

Clearing the annotation for a property will cause any associated resources to be released. If a callback property server was used (see <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropserver">SetPropServer</a>), it will be released.