---
UID: NF:oleacc.IAccPropServices.ClearHmenuProps
title: IAccPropServices::ClearHmenuProps (oleacc.h)
description: This method wraps ClearProps, and provides a convenient entry point for callers who are annotating HMENU-based accessible elements.
helpviewer_keywords: ["ClearHmenuProps","ClearHmenuProps method [Windows Accessibility]","ClearHmenuProps method [Windows Accessibility]","IAccPropServices interface","IAccPropServices interface [Windows Accessibility]","ClearHmenuProps method","IAccPropServices.ClearHmenuProps","IAccPropServices::ClearHmenuProps","oleacc/IAccPropServices::ClearHmenuProps","winauto.iaccpropservices_iaccpropservices__clearhmenuprops"]
old-location: winauto\iaccpropservices_iaccpropservices__clearhmenuprops.htm
tech.root: WinAuto
ms.assetid: dbff74b0-c67b-4ef4-add7-6063c4760455
ms.date: 12/05/2018
ms.keywords: ClearHmenuProps, ClearHmenuProps method [Windows Accessibility], ClearHmenuProps method [Windows Accessibility],IAccPropServices interface, IAccPropServices interface [Windows Accessibility],ClearHmenuProps method, IAccPropServices.ClearHmenuProps, IAccPropServices::ClearHmenuProps, oleacc/IAccPropServices::ClearHmenuProps, winauto.iaccpropservices_iaccpropservices__clearhmenuprops
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
 - IAccPropServices::ClearHmenuProps
 - oleacc/IAccPropServices::ClearHmenuProps
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
 - IAccPropServices.ClearHmenuProps
---

# IAccPropServices::ClearHmenuProps


## -description

This method wraps  <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a>, and provides a convenient entry point for callers who are annotating <b>HMENU</b>-based accessible elements.

## -parameters

### -param hmenu [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMENU</a></b>

Identifies the <b>HMENU</b>-based accessible element to be annotated.

### -param idChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the child ID of the accessible element.

### -param paProps [in]

Type: <b>const MSAAPROPID*</b>

Specifies an array of properties to be reset. These properties will revert to the default behavior that they displayed before they were annotated.

### -param cProps [in]

Type: <b>int</b>

Specifies the number of properties in the <i>paProps</i> array.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK, even if the specified properties were never annotated on the accessible object; clearing already-cleared properties is considered a success.

Returns E_INVALIDARG if any of the properties in the <i>paProps</i> array are not supported.

May return other error codes under exceptional error conditions such as low memory.

For descriptions of other parameters and return values, see the <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a> method.

## -remarks

By using this method, the caller does not have to obtain an identity string; it can specify the <i>hmenu</i> and <i>idChild</i> parameters directly.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearprops">ClearProps</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices">IAccPropServices</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethmenuprop">SetHmenuProp</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethmenupropserver">SetHmenuPropServer</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethmenupropstr">SetHmenuPropStr</a>