---
UID: NF:oleacc.IAccessible.accSelect
title: IAccessible::accSelect (oleacc.h)
description: The IAccessible::accSelect method modifies the selection or moves the keyboard focus of the specified object. All objects that support selection or receive the keyboard focus must support this method.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","accSelect method","IAccessible.accSelect","IAccessible::accSelect","_msaa_IAccessible_accSelect","accSelect","accSelect method [Windows Accessibility]","accSelect method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__accselect","oleacc/IAccessible::accSelect","winauto.iaccessible_iaccessible__accselect"]
old-location: winauto\iaccessible_iaccessible__accselect.htm
tech.root: WinAuto
ms.assetid: ae55831c-0dfa-4901-b241-27e2cdf1035f
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],accSelect method, IAccessible.accSelect, IAccessible::accSelect, _msaa_IAccessible_accSelect, accSelect, accSelect method [Windows Accessibility], accSelect method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__accselect, oleacc/IAccessible::accSelect, winauto.iaccessible_iaccessible__accselect
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
 - IAccessible::accSelect
 - oleacc/IAccessible::accSelect
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
 - IAccessible.accSelect
---

# IAccessible::accSelect


## -description

The <b>IAccessible::accSelect</b> method modifies the selection or moves the keyboard focus of the specified object. All objects that support selection or receive the keyboard focus must support this method.

## -parameters

### -param flagsSelect [in]

Type: <b>long</b>

Specifies which selection or focus operations are to be performed. This parameter must have a combination of the <a href="/windows/desktop/WinAuto/selflag">SELFLAG Constants</a>.

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies the selected object. If the value is CHILDID_SELF, the object itself is selected; if a child ID, one of the object's child elements is selected. For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified object is not selected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument is not valid. This return value means that the specified SELFLAG combination is not valid, or that the SELFLAG value does not make sense for the specified object. For example, the following flags are not allowed on a single-selection list box: <a href="/windows/desktop/WinAuto/selflag">SELFLAG_EXTENDSELECTION</a>, <a href="/windows/desktop/WinAuto/selflag">SELFLAG_ADDSELECTION</a>, and <a href="/windows/desktop/WinAuto/selflag">SELFLAG_REMOVESELECTION</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this method.

</td>
</tr>
</table>

## -remarks

Client applications use this method to perform complex selection operations. For more information, see <a href="/windows/desktop/WinAuto/selecting-child-objects">Selecting Child Objects</a>. This method provides the simplest way to programmatically switch the input focus between applications. This applies to applications running on Windows 2000.

<b>Note:  </b>This method is for the selection of items, not text.
            

<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function selects the item at a specified point on the screen. It is assumed that a single selection is wanted.


```cpp

HRESULT SelectItemAtPoint(POINT point)
{
    VARIANT varItem;
    IAccessible* pAcc;
    HRESULT hr = AccessibleObjectFromPoint(point, &pAcc, &varItem);
    if ((hr == S_OK))
    {
        hr = pAcc->accSelect((SELFLAG_TAKEFOCUS | SELFLAG_TAKESELECTION), varItem);
        VariantClear(&varItem);
        pAcc->Release();
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accfocus">IAccessible::get_accFocus</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accselection">IAccessible::get_accSelection</a>



<a href="/windows/desktop/WinAuto/selflag">SELFLAG</a>



<a href="/windows/desktop/WinAuto/selection-and-focus-properties-and-methods">Selection and Focus Properties and Methods</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>