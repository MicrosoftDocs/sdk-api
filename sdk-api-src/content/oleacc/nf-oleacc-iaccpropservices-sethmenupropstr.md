---
UID: NF:oleacc.IAccPropServices.SetHmenuPropStr
title: IAccPropServices::SetHmenuPropStr (oleacc.h)
description: This method wraps SetPropValue, providing a more convenient entry point for callers who are annotating HMENU-based accessible elements.
helpviewer_keywords: ["IAccPropServices interface [Windows Accessibility]","SetHmenuPropStr method","IAccPropServices.SetHmenuPropStr","IAccPropServices::SetHmenuPropStr","SetHmenuPropStr","SetHmenuPropStr method [Windows Accessibility]","SetHmenuPropStr method [Windows Accessibility]","IAccPropServices interface","oleacc/IAccPropServices::SetHmenuPropStr","winauto.iaccpropservices_iaccpropservices__sethmenupropstr"]
old-location: winauto\iaccpropservices_iaccpropservices__sethmenupropstr.htm
tech.root: WinAuto
ms.assetid: 891af40a-819b-4fce-a1bb-28db145b87f1
ms.date: 12/05/2018
ms.keywords: IAccPropServices interface [Windows Accessibility],SetHmenuPropStr method, IAccPropServices.SetHmenuPropStr, IAccPropServices::SetHmenuPropStr, SetHmenuPropStr, SetHmenuPropStr method [Windows Accessibility], SetHmenuPropStr method [Windows Accessibility],IAccPropServices interface, oleacc/IAccPropServices::SetHmenuPropStr, winauto.iaccpropservices_iaccpropservices__sethmenupropstr
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
 - IAccPropServices::SetHmenuPropStr
 - oleacc/IAccPropServices::SetHmenuPropStr
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
 - IAccPropServices.SetHmenuPropStr
---

# IAccPropServices::SetHmenuPropStr


## -description

This method wraps <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>, providing a more convenient entry point for callers who are annotating <b>HMENU</b>-based accessible elements.

## -parameters

### -param hmenu [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HMENU</a></b>

Identifies the <b>HMENU</b>-based accessible element to be annotated.

### -param idChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Specifies the child ID of the accessible element.

### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies which property of the accessible element is to be annotated.

### -param str [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

Specifies a new value for the <i>idProp</i> property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

May return other error codes under exceptional error conditions such as low memory.

## -remarks

By using this method, the caller does not have to obtain an identity string; it can specify the <i>hmenu</i>, <i>idObject</i>, and <i>idChild</i> parameters directly.

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-clearhmenuprops">ClearHmenuProps</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices">IAccPropServices</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethmenuprop">SetHmenuProp</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-sethmenupropserver">SetHmenuPropServer</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccpropservices-setpropvalue">SetPropValue</a>