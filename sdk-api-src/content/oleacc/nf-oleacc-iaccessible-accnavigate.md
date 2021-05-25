---
UID: NF:oleacc.IAccessible.accNavigate
title: IAccessible::accNavigate (oleacc.h)
description: The IAccessible::accNavigate method traverses to another UI element within a container and retrieves the object. This method is optional.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","accNavigate method","IAccessible.accNavigate","IAccessible::accNavigate","VT_DISPATCH","VT_EMPTY","VT_I4","_msaa_IAccessible_accNavigate","accNavigate","accNavigate method [Windows Accessibility]","accNavigate method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__accnavigate","oleacc/IAccessible::accNavigate","winauto.iaccessible_iaccessible__accnavigate"]
old-location: winauto\iaccessible_iaccessible__accnavigate.htm
tech.root: WinAuto
ms.assetid: 8825c951-a6c1-4690-b36a-6159f30a13d9
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],accNavigate method, IAccessible.accNavigate, IAccessible::accNavigate, VT_DISPATCH, VT_EMPTY, VT_I4, _msaa_IAccessible_accNavigate, accNavigate, accNavigate method [Windows Accessibility], accNavigate method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__accnavigate, oleacc/IAccessible::accNavigate, winauto.iaccessible_iaccessible__accnavigate
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
 - IAccessible::accNavigate
 - oleacc/IAccessible::accNavigate
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
 - IAccessible.accNavigate
---

# IAccessible::accNavigate


## -description

The <b>IAccessible::accNavigate</b> method traverses to another UI element within a container and retrieves the object. This method is optional.
<div class="alert"><b>Note</b>  The <b>accNavigate</b> method is deprecated and should not be used. Clients should use other methods and properties such as <a href="/windows/desktop/api/oleacc/nf-oleacc-accessiblechildren">AccessibleChildren</a>, <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">get_accChild</a>, <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accparent">get_accParent</a>, and <a href="/windows/win32/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>.</div><div> </div>

## -parameters

### -param navDir [in]

Type: <b>long</b>

Specifies the direction to navigate. This direction is in <i>spatial</i> order, such as left or right, or <i>logical</i> order, such as next or previous. This value is one of the <a href="/windows/desktop/WinAuto/navigation-constants">navigation constants</a>.

### -param varStart [in]

Type: <b>VARIANT</b>

Specifies whether the starting object of the navigation is the object itself or one of the object's children. This parameter is either CHILDID_SELF (to start from the object) or a child ID (to start from one of the object's child elements). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pvarEndUpAt [out, retval]

Type: <b>VARIANT*</b>

[out, retval] Address of a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> structure that receives information about the destination object. The following table describes the information that is returned in <i>pvarEnd</i>.

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
None. There was no UI element in the specified direction.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_I4"></a><a id="vt_i4"></a><dl>
<dt><b>VT_I4</b></dt>
</dl>
</td>
<td width="60%">
<b>lVal</b> contains the child ID of the UI element.

</td>
</tr>
<tr>
<td width="40%"><a id="VT_DISPATCH"></a><a id="vt_dispatch"></a><dl>
<dt><b>VT_DISPATCH</b></dt>
</dl>
</td>
<td width="60%">
<b>pdispVal</b> contains the address of the UI element's <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="/windows/desktop/WinAuto/checking-iaccessible-return-values">Checking IAccessible Return Values</a> and Return Values.

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
No screen element was found in the specified direction.

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

Navigation, both spatial and logical, is always restricted to the UI elements within a container. With spatial navigation, clients navigate only to a sibling of the starting object (<i>varStart</i>). Depending on the navigational flag used with logical navigation, clients navigate to either a child or to a sibling of the starting object.

The <b>accNavigate</b> method retrieves UI elements that have a defined screen location, and invisible objects that do not have a defined screen location.

This method does not change the selection or focus. To change the focus or to select an object, use <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accselect">IAccessible::accSelect</a>.

To prevent looping when traversing screen elements, <b>accNavigate</b> returns S_FALSE with VT_EMPTY when you specify <a href="/windows/desktop/WinAuto/navigation-constants">NAVDIR_NEXT</a> on the last element, or <a href="/windows/desktop/WinAuto/navigation-constants">NAVDIR_PREVIOUS</a> on the first element.

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.

Some system-defined UI elements such as menus, menu items, and pop-up menus allow navigation to invisible objects. However, other system-defined UI elements do not support this. Servers can choose whether to support navigating to invisible objects and can either skip over or expose them.

Client applications must return post-process return values when using <b>accNavigate</b> to navigate between objects. The goal of the post-processing steps is to give clients an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer and a child ID so that they can use the <b>IAccessible</b> methods and properties for a UI element.

The following tables describe possible scenarios for <b>IAccessible::accNavigate</b>, based on the following criteria:

<ul>
<li>A defined starting point (whether you are starting with a full object or a simple element)</li>
<li> 
The result returned (an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> or a VT_I4 child ID)</li>
<li> 
The post-processing that client applications will need to perform to have an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer and a child ID </li>
</ul>
For these tables, assume that <i>startID</i> and <i>endID</i> are VT_I4 child IDs (simple elements), and <i>pStartAcc</i> and <i>pEndAcc</i> are VT_I4 with CHILDID_SELF (full objects).

This table describes the following NAVDIR_ flags: NEXT, PREVIOUS, LEFT, RIGHT, UP, and DOWN. For more information about navigation flags, see <a href="/windows/desktop/WinAuto/navigation-constants">Navigation Constants</a>.

<table>
<tr>
<th>Starting point</th>
<th>Result returned</th>
<th>Post-processing for the return value</th>
</tr>
<tr>
<td><i>pStartAcc, startID</i></td>
<td>VT_I4 <i>endID</i></td>
<td>Call <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">get_accChild</a> on <i>pStartAcc</i> passing <i>endID</i>. Follow normal procedures outlined in <b>get_accChild</b>.</td>
</tr>
<tr>
<td><i>pStartAcc, startID</i></td>
<td>VT_DISPATCH <i>pEndAcc</i></td>
<td> Use the standard procedures for converting an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface pointer to an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer for <i>pEndAcc</i>.  </td>
</tr>
<tr>
<td><i>pStartAcc</i>, CHILDID_SELF</td>
<td>VT_I4 <i>endID</i></td>
<td>Call <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accparent">get_accParent</a> on <i>pStartAcc</i>, passing CHILDID_SELF to get the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer of the parent for <i>endID</i>. 
Then, call <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">get_accChild</a> on that <b>IAccessible</b> interface pointer, passing <i>endID</i>. Follow normal procedures outlined in <b>get_accChild</b>.</td>
</tr>
<tr>
<td><i>pStartAcc</i>, CHILDID_SELF</td>
<td>VT_DISPATCH <i>pEndAcc</i></td>
<td>Use the standard procedures for converting an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface pointer to an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer for <i>pEndAcc</i>.</td>
</tr>
</table>
 

The following table describes navigation flags <a href="/windows/desktop/WinAuto/navigation-constants">NAVDIR_FIRSTCHILD</a> and <a href="/windows/desktop/WinAuto/navigation-constants">NAVDIR_LASTCHILD</a>. It does not include entries for navigating to a first or last child when the starting point is a simple element because simple elements cannot have children.

<table>
<tr>
<th>Starting point</th>
<th>Result returned</th>
<th>Post-processing for the return value</th>
</tr>
<tr>
<td><i>pStartAcc</i>, CHILDID_SELF</td>
<td>VT_I4 <i>endID</i></td>
<td>Call <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accchild">get_accChild</a> on <i>pStartAcc</i>, passing endID. Follow normal procedures outlined in <b>get_accChild</b>. </td>
</tr>
<tr>
<td><i>pStartAcc</i>, CHILDID_SELF</td>
<td>VT_DISPATCH <i>pEndAcc</i></td>
<td>Use the standard procedures for converting an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface pointer to an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointer for <i>pEndAcc</i>.</td>
</tr>
</table>
 

For more information, see <a href="/windows/desktop/WinAuto/object-navigation-properties-and-methods">Object Navigation Properties and Methods</a>.

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example shows a possible implementation of the method for a custom list box whose list items are child elements.


```cpp

// m_pControl is the control that returns this accessible object. 
// m_pStdAccessibleObject is the standard accessible object for the window 
//    that contains the control. 

HRESULT STDMETHODCALLTYPE AccServer::accNavigate( 
    long navDir,
    VARIANT varStart,
    VARIANT *pvarEndUpAt)
{
    // Default value. 
    pvarEndUpAt->vt = VT_EMPTY;

    if (varStart.vt != VT_I4)
    {
        return E_INVALIDARG;
    }

    switch (navDir)
    {
    case NAVDIR_FIRSTCHILD:
        if (varStart.lVal == CHILDID_SELF)
        {
            pvarEndUpAt->vt = VT_I4;
            pvarEndUpAt->lVal = 1;
        }
        else  // Starting with child. 
        {
            return S_FALSE;
        }
        break;

    case NAVDIR_LASTCHILD:
        if (varStart.lVal == CHILDID_SELF)
        {
            pvarEndUpAt->vt = VT_I4;
            pvarEndUpAt->lVal = m_pControl->GetCount();
        }
        else  // Starting with child.           
        {
            return S_FALSE;
        }
        break;

    case NAVDIR_NEXT:   
    case NAVDIR_DOWN:
        if (varStart.lVal != CHILDID_SELF)
        {
            pvarEndUpAt->vt = VT_I4;
            pvarEndUpAt->lVal = varStart.lVal + 1;
            // Out of range. 
            if (pvarEndUpAt->lVal > m_pControl->GetCount())
            {
                pvarEndUpAt->vt = VT_EMPTY;
                return S_FALSE;
            }
        }
        else  // Call through to method on standard object. 
        {
            return m_pStdAccessibleObject->accNavigate(navDir, varStart, pvarEndUpAt);
        }
        break;

    case NAVDIR_PREVIOUS:
    case NAVDIR_UP:
        if (varStart.lVal != CHILDID_SELF)
        {
            pvarEndUpAt->vt = VT_I4;
            pvarEndUpAt->lVal = varStart.lVal - 1;
            // Out of range. 
            if (pvarEndUpAt->lVal <1)
            {
                pvarEndUpAt->vt = VT_EMPTY;
                return S_FALSE;
            }
        }
        else  // Call through to method on standard object. 
        {
            return m_pStdAccessibleObject->accNavigate(navDir, varStart, pvarEndUpAt);
        }
        break;

     // Unsupported directions. 
    case NAVDIR_LEFT:
    case NAVDIR_RIGHT:
        if (varStart.lVal == CHILDID_SELF)
        {
            return m_pStdAccessibleObject->accNavigate(navDir, varStart, pvarEndUpAt);
        }
        else 
        {
            pvarEndUpAt->vt = VT_EMPTY;
            return S_FALSE;
        }
        break;
    }
    return S_OK;
};


```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accselect">IAccessible::accSelect</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/object-navigation-properties-and-methods">Object Navigation Properties and Methods</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>