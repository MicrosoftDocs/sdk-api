---
UID: NF:oleacc.IAccessible.get_accValue
title: IAccessible::get_accValue (oleacc.h)
description: The IAccessible::get_accValue method retrieves the value of the specified object. Not all objects have a value.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accValue method","IAccessible.get_accValue","IAccessible::get_accValue","_msaa_IAccessible_get_accValue","get_accValue","get_accValue method [Windows Accessibility]","get_accValue method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accvalue","oleacc/IAccessible::get_accValue","winauto.iaccessible_iaccessible__get_accvalue"]
old-location: winauto\iaccessible_iaccessible__get_accvalue.htm
tech.root: WinAuto
ms.assetid: 8e29adec-13fb-4a85-87ac-9e8034dce147
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accValue method, IAccessible.get_accValue, IAccessible::get_accValue, _msaa_IAccessible_get_accValue, get_accValue, get_accValue method [Windows Accessibility], get_accValue method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accvalue, oleacc/IAccessible::get_accValue, winauto.iaccessible_iaccessible__get_accvalue
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
 - IAccessible::get_accValue
 - oleacc/IAccessible::get_accValue
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
 - IAccessible.get_accValue
---

# IAccessible::get_accValue


## -description

The <b>IAccessible::get_accValue</b> method retrieves the value of the specified object. Not all objects have a value.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved value information belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pszValue [out, retval]

Type: <b>BSTR*</b>

 Address of the <b>BSTR</b> that receives a localized string that contains the object's current value.

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

Numeric values returned from scroll bar and trackbar accessible objects indicate percentages. They are integers between zero (0) and one hundred (100), inclusive, but might also be a limited range for example, between one (1) and sixteen (16). Also, some scroll bar and trackbar objects return strings that correspond to settings such as screen size or Internet security.

<b>Note to server developers:  </b>Localize the string returned from this property.

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/WinAuto/value-property">Value Property</a>