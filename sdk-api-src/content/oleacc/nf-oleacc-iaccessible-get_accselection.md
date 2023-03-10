---
UID: NF:oleacc.IAccessible.get_accSelection
title: IAccessible::get_accSelection (oleacc.h)
description: The IAccessible::get_accSelection method retrieves the selected children of this object. All objects that support selection must support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accSelection method","IAccessible.get_accSelection","IAccessible::get_accSelection","VT_DISPATCH","VT_EMPTY","VT_I4","VT_UNKNOWN","_msaa_IAccessible_get_accSelection","get_accSelection","get_accSelection method [Windows Accessibility]","get_accSelection method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accselection","oleacc/IAccessible::get_accSelection","winauto.iaccessible_iaccessible__get_accselection"]
old-location: winauto\iaccessible_iaccessible__get_accselection.htm
tech.root: WinAuto
ms.assetid: 80df32de-a99f-4a5a-b354-f3e133f3e620
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accSelection method, IAccessible.get_accSelection, IAccessible::get_accSelection, VT_DISPATCH, VT_EMPTY, VT_I4, VT_UNKNOWN, _msaa_IAccessible_get_accSelection, get_accSelection, get_accSelection method [Windows Accessibility], get_accSelection method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accselection, oleacc/IAccessible::get_accSelection, winauto.iaccessible_iaccessible__get_accselection
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
 - IAccessible::get_accSelection
 - oleacc/IAccessible::get_accSelection
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
 - IAccessible.get_accSelection
---

# IAccessible::get_accSelection


## -description

The <b>IAccessible::get_accSelection</b> method retrieves the selected children of this object. All objects that support selection must support this property.

## -parameters

### -param pvarChildren [out, retval]

Type: <b>VARIANT*</b>

Address of a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a> that receives information about which children are selected. The following table describes the information returned in <i>pvarChildren</i>.

<table>
<tr>
<th>vt member</th>
<th>Value member</th>
</tr>
<tr>
<td width="40%"><a id="VT_EMPTY"></a><a id="vt_empty"></a><dl>
<dt><b>VT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
No children are selected.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_DISPATCH"></a><a id="vt_dispatch"></a><dl>
<dt><b>VT_DISPATCH</b></dt>
</dl>
</td>
<td width="60%">
One child object is selected, and the address of its <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface is set in the <b>pdispVal</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_I4"></a><a id="vt_i4"></a><dl>
<dt><b>VT_I4</b></dt>
</dl>
</td>
<td width="60%">
<b>lVal</b> contains the child ID of the child element that is selected. If <b>lVal</b> is CHILDID_SELF, this means that the object itself is selected.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_UNKNOWN"></a><a id="vt_unknown"></a><dl>
<dt><b>VT_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
Multiple child objects are selected, and the <b>punkVal</b> member contains the address of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. The client queries this interface for the <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface, which it uses to enumerate the selected objects.

</td>
</tr>
</table>

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
</table>

## -remarks

This method must support the <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface.

This method returns either an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface pointer or a child ID for the <i>pvarChildren</i> parameter. For more information about how to use the <b>IDispatch</b> interface pointer or child ID, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.

<b>Note:  </b>This method retrieves a selected item, not selected text.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows a possible implementation of this method for a custom single-selection list box. Its  <b>GetSelectedIndex</b> method returns -1 if no item is selected.


```cpp

// m_pControl is the control that returns this accessible object. 

HRESULT STDMETHODCALLTYPE AccServer::get_accSelection(VARIANT *pvarChildren)
{
    int childID = m_pControl->GetSelectedIndex() + 1; // Convert from 0-based. 
    if (childID <= 0)
    {
        pvarChildren->vt = VT_EMPTY;
    }
    else 
    {
        pvarChildren->vt = VT_I4;
        pvarChildren->lVal = childID;
    }
    return S_OK;
};




```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accselect">IAccessible::accSelect</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accfocus">IAccessible::get_accFocus</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/selection-and-focus-properties-and-methods">Selection and Focus Properties and Methods</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>