---
UID: NF:oleacc.IAccessible.accHitTest
title: IAccessible::accHitTest (oleacc.h)
description: The IAccessible::accHitTest method retrieves the child element or child object that is displayed at a specific point on the screen.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","accHitTest method","IAccessible.accHitTest","IAccessible::accHitTest","_msaa_IAccessible_accHitTest","accHitTest","accHitTest method [Windows Accessibility]","accHitTest method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__acchittest","oleacc/IAccessible::accHitTest","winauto.iaccessible_iaccessible__acchittest"]
old-location: winauto\iaccessible_iaccessible__acchittest.htm
tech.root: WinAuto
ms.assetid: 87327086-a8f3-4d1c-ab4d-8f5aba00c61a
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],accHitTest method, IAccessible.accHitTest, IAccessible::accHitTest, _msaa_IAccessible_accHitTest, accHitTest, accHitTest method [Windows Accessibility], accHitTest method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__acchittest, oleacc/IAccessible::accHitTest, winauto.iaccessible_iaccessible__acchittest
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
 - IAccessible::accHitTest
 - oleacc/IAccessible::accHitTest
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
 - IAccessible.accHitTest
---

# IAccessible::accHitTest


## -description

The <b>IAccessible::accHitTest</b> method retrieves the child element or child object that is displayed at a specific point on the screen. All visual objects support this method, but sound objects do not. Client applications rarely call this method directly; to get the accessible object that is displayed at a point, use the <a href="/windows/desktop/api/oleacc/nf-oleacc-accessibleobjectfrompoint">AccessibleObjectFromPoint</a> function, which calls this method internally.

## -parameters

### -param xLeft [in]

Type: <b>long</b>

Specifies the screen coordinates of the point that is hit tested. The x-coordinates increase from left to right. Note that when screen coordinates are used, the origin is the upper-left corner of the screen.

### -param yTop [in]

Type: <b>long</b>

Specifies the screen coordinates of the point that is hit tested. The y-coordinates increase from top to bottom. Note that when screen coordinates are used, the origin is the upper-left corner of the screen.

### -param pvarChild [out, retval]

Type: <b>VARIANT*</b>

[out, retval] Address of a <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a> that identifies the object displayed at the point specified by <i>xLeft</i> and <i>yTop</i>. The information returned in <i>pvarID</i> depends on the location of the specified point in relation to the object whose <b>accHitTest</b> method is being called.

<table>
<tr>
<th>Point location</th>
<th>vt member</th>
<th>Value member</th>
</tr>
<tr>
<td>Outside of the object's boundaries, and either inside or outside of the object's bounding rectangle.</td>
<td>VT_EMPTY</td>
<td>None.</td>
</tr>
<tr>
<td>Within the object but not within a child element or a child object.</td>
<td>VT_I4</td>
<td><b>lVal</b> is CHILDID_SELF.</td>
</tr>
<tr>
<td>Within a child element.</td>
<td>VT_I4</td>
<td><b>lVal</b> contains the child ID.</td>
</tr>
<tr>
<td>Within a child object.</td>
<td>VT_DISPATCH</td>
<td><i>pdispVal</i> is set to the child object's <a href="/windows/win32/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer</td>
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
The point is outside of the object's boundaries. The <b>vt</b> member of <i>pvarID</i> is VT_EMPTY.

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
 

<b>Note to client developers:  </b>Although servers return S_FALSE if the <b>vt</b> member of <i>pvarID</i> is VT_EMPTY, clients must also handle the case where <i>pvarID</i>-&gt;vt is VT_EMPTY and the return value is S_OK.

## -remarks

If the tested point is on one of the object's children, and this child supports the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface itself, this method should return an <b>IAccessible</b> interface pointer. However, clients should be prepared to handle an <b>IAccessible</b> interface pointer or a child ID. For more information, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

Because <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-acclocation">accLocation</a> returns a bounding rectangle, not all points in that rectangle will be within the actual bounds of the object. Some points within the bounding rectangle may not be on the object. For non-rectangular objects, such as list view items in large-icon mode where a single item has a rectangle for the icon and another rectangle for the text of the icon, the coordinates of the object's bounding rectangle retrieved by <b>IAccessible::accLocation</b> could fail if tested with <b>accHitTest</b> .

As with other <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="/windows/desktop/WinAuto/receiving-errors-for-iaccessible-interface-pointers">Receiving Errors for IAccessible Interface Pointers</a>.

When this method is used in certain situations, additional usage notes apply. For more information, see <a href="/windows/desktop/WinAuto/navigation-through-hit-testing-and-screen-location">Navigation Through Hit Testing and Screen Location</a>.

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows a possible implementation for a custom list box.


```cpp

// m_pControl is the control that returns this accessible object. 
// m_hwnd is the HWND of the control window. 
//  
HRESULT STDMETHODCALLTYPE AccServer::accHitTest( 
    long xLeft,
    long yTop,
    VARIANT *pvarChild) 

{
    POINT pt;
    pt.x = xLeft;
    pt.y = yTop;

    // Not in our window. 
    if (WindowFromPoint(pt) != m_hwnd)
    {
        pvarChild->vt = VT_EMPTY;
        return S_FALSE;
    }

    else  // In our window; return list item, or self if in blank space. 
    {
        pvarChild->vt = VT_I4;
        ScreenToClient(m_hwnd, &pt);
        // IndexFromY returns the 0-based index of the item at that point, 
        // or -1 if the point is not on any item.
        int index = m_pControl->IndexFromY(pt.y);
        if (index >= 0)
        {
            // Increment, because the child array is 1-based. 
            pvarChild->lVal = index + 1;
        }
        else
        {
            pvarChild->lVal = CHILDID_SELF;

        }
        return S_OK;
    }
};

```


<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function selects the item at a specified point on the screen within the list represented by <i>pAcc</i>. It is assumed that a single selection is wanted.


```cpp

HRESULT SelectItemAtPoint(IAccessible* pAcc, POINT point)
{
    if (pAcc == NULL)
    {
        return E_INVALIDARG;
    }
    VARIANT varChild;

    HRESULT hr = pAcc->accHitTest(point.x, point.y, &varChild);        
    if ((hr == S_OK) && (varChild.lVal != CHILDID_SELF))
    {
        return pAcc->accSelect((SELFLAG_TAKEFOCUS | SELFLAG_TAKESELECTION), varChild);
    }
    return S_FALSE;
}

```

## -see-also

<a href="/windows/desktop/WinAuto/active-accessibility-and-windows-vista-screen-scaling">Active Accessibility and Windows Vista Screen Scaling</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-acclocation">IAccessible::accLocation</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/navigation-through-hit-testing-and-screen-location">Navigation Through Hit Testing and Screen Location</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>