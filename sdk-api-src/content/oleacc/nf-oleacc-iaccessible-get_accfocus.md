---
UID: NF:oleacc.IAccessible.get_accFocus
title: IAccessible::get_accFocus (oleacc.h)
description: The IAccessible::get_accFocus method retrieves the object that has the keyboard focus. All objects that may receive the keyboard focus must support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accFocus method","IAccessible.get_accFocus","IAccessible::get_accFocus","VT_DISPATCH","VT_EMPTY","VT_I4","_msaa_IAccessible_get_accFocus","get_accFocus","get_accFocus method [Windows Accessibility]","get_accFocus method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accfocus","oleacc/IAccessible::get_accFocus","winauto.iaccessible_iaccessible__get_accfocus"]
old-location: winauto\iaccessible_iaccessible__get_accfocus.htm
tech.root: WinAuto
ms.assetid: 42114c5d-8f28-458a-8d22-ac1531cd50d2
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accFocus method, IAccessible.get_accFocus, IAccessible::get_accFocus, VT_DISPATCH, VT_EMPTY, VT_I4, _msaa_IAccessible_get_accFocus, get_accFocus, get_accFocus method [Windows Accessibility], get_accFocus method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accfocus, oleacc/IAccessible::get_accFocus, winauto.iaccessible_iaccessible__get_accfocus
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
 - IAccessible::get_accFocus
 - oleacc/IAccessible::get_accFocus
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
 - IAccessible.get_accFocus
---

# IAccessible::get_accFocus


## -description

The <b>IAccessible::get_accFocus</b> method retrieves the object that has the keyboard focus. All objects that may receive the keyboard focus must support this property.

## -parameters

### -param pvarChild [out, retval]

Type: <b>VARIANT*</b>

Address of a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a> that receives information about the object that has the focus. The following table describes the information returned in <i>pvarID</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VT_EMPTY"></a><a id="vt_empty"></a><dl>
<dt><b>VT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
None. Neither this object nor any of its children has the keyboard focus.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_I4"></a><a id="vt_i4"></a><dl>
<dt><b>VT_I4</b></dt>
</dl>
</td>
<td width="60%">
<b>lVal</b> is CHILDID_SELF. The object itself has the keyboard focus.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_I4"></a><a id="vt_i4"></a><dl>
<dt><b>VT_I4</b></dt>
</dl>
</td>
<td width="60%">
<b>lVal</b> contains the child ID of the child element that has the keyboard focus.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_DISPATCH"></a><a id="vt_dispatch"></a><dl>
<dt><b>VT_DISPATCH</b></dt>
</dl>
</td>
<td width="60%">
<b>pdispVal</b> member is the address of the <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch interface</a> for the child object that has the keyboard focus.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object is a window but not the foreground window.

</td>
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

The concept of keyboard focus is related to that of an active window. An active window is the foreground window on which the user works. The object with the keyboard focus is either the active window or a child object of the active window.

Only one object or item within a container has the focus at any one time. The object with the keyboard focus is not always the selected object. For more information about the difference between selection and focus, see <a href="/windows/desktop/WinAuto/selection-and-focus-properties-and-methods">Selection and Focus Properties and Methods</a>.

This method returns either an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface pointer or a child ID for the <i>pvarID</i>. For more information about how to use the <b>IDispatch</b> interface pointer or child ID, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows a possible implementation of this method for a custom single-selection list box. If the control does not have the focus, VT_EMPTY is returned in the variant by the standard accessible object for the HWND. If the control does have the focus, and an item is selected, the child ID of that item is returned; if there is no selection, CHILDID_SELF is returned.


```cpp

// m_pControl is the control object that is served by this implementation. 
// m_pStdAccessibleObject is the object returned by CreateStdAccessibleObject. 

HRESULT STDMETHODCALLTYPE AccServer::get_accFocus(VARIANT *pvarChild)
{
    FAIL_IF_NO_CONTROL;  // Macro that checks for existence of control. 

    HRESULT hr = m_pStdAccessibleObject->get_accFocus(pvarChild);  
    if (pvarChild->vt != VT_I4)
    {
        return hr;
    }
    else
    {
        int index = m_pControl->GetSelectedIndex();
        if (index <0)
        {
            pvarChild->lVal = CHILDID_SELF;
        }
        else
        {
            // Convert to 1-based index for child ID. 
            pvarChild->lVal = index + 1;
        }
    }
    return S_OK;
};


```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accselect">IAccessible::accSelect</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accselection">IAccessible::get_accSelection</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/selection-and-focus-properties-and-methods">Selection and Focus Properties and Methods</a>