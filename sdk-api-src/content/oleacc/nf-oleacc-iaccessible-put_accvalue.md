---
UID: NF:oleacc.IAccessible.put_accValue
title: IAccessible::put_accValue (oleacc.h)
description: The IAccessible::put_accValue method sets the value of the specified object. Not all objects have a value.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","put_accValue method","IAccessible.put_accValue","IAccessible::put_accValue","_msaa_IAccessible_put_accValue","msaa.iaccessible_iaccessible__put_accvalue","oleacc/IAccessible::put_accValue","put_accValue","put_accValue method [Windows Accessibility]","put_accValue method [Windows Accessibility]","IAccessible interface","winauto.iaccessible_iaccessible__put_accvalue"]
old-location: winauto\iaccessible_iaccessible__put_accvalue.htm
tech.root: WinAuto
ms.assetid: 0b1e44f4-8d03-47a4-a8c5-5296059e0459
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],put_accValue method, IAccessible.put_accValue, IAccessible::put_accValue, _msaa_IAccessible_put_accValue, msaa.iaccessible_iaccessible__put_accvalue, oleacc/IAccessible::put_accValue, put_accValue, put_accValue method [Windows Accessibility], put_accValue method [Windows Accessibility],IAccessible interface, winauto.iaccessible_iaccessible__put_accvalue
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - IAccessible::put_accValue
 - oleacc/IAccessible::put_accValue
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
 - IAccessible.put_accValue
---

# IAccessible::put_accValue


## -description

The <b>IAccessible::put_accValue</b> method sets the value of the specified object. Not all objects have a value.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the value information being set belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to set information on the object) or a child ID (to set information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param szValue [in]

Type: <b>BSTR</b>

A localized string that contains the object's value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="/windows/desktop/WinAuto/checking-iaccessible-return-values">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid.

</td>
</tr>
</table>

## -remarks

The <b>IAccessible::put_accValue</b> method is supported for some UI elements (usually edit controls). For UI elements that do not support this method, control-specific methods are used instead. For more information, see <a href="/windows/desktop/WinAuto/appendix-a--supported-user-interface-elements-reference">Supported User Interface Element Reference</a>.