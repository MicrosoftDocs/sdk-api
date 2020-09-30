---
UID: NF:oleacc.IAccessible.accLocation
title: IAccessible::accLocation (oleacc.h)
description: The IAccessible::accLocation method retrieves the specified object's current screen location. All visual objects must support this method. Sound objects do not support this method.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","accLocation method","IAccessible.accLocation","IAccessible::accLocation","_msaa_IAccessible_accLocation","accLocation","accLocation method [Windows Accessibility]","accLocation method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__acclocation","oleacc/IAccessible::accLocation","winauto.iaccessible_iaccessible__acclocation"]
old-location: winauto\iaccessible_iaccessible__acclocation.htm
tech.root: WinAuto
ms.assetid: 1eb6f075-a8bf-4c03-96ee-460728317955
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],accLocation method, IAccessible.accLocation, IAccessible::accLocation, _msaa_IAccessible_accLocation, accLocation, accLocation method [Windows Accessibility], accLocation method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__acclocation, oleacc/IAccessible::accLocation, winauto.iaccessible_iaccessible__acclocation
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
 - IAccessible::accLocation
 - oleacc/IAccessible::accLocation
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
 - IAccessible.accLocation
---

# IAccessible::accLocation


## -description

The <b>IAccessible::accLocation</b> method retrieves the specified object's current screen location. All visual objects must support this method. Sound objects do not support this method.

## -parameters

### -param pxLeft [out]

Type: <b>long*</b>

Address, in physical screen coordinates, of the variable that receives the x-coordinate of the upper-left boundary of the object's location.

### -param pyTop [out]

Type: <b>long*</b>

Address, in physical screen coordinates, of the variable that receives the y-coordinate of the upper-left boundary of the object's location.

### -param pcxWidth [out]

Type: <b>long*</b>

Address, in pixels, of the variable that receives the object's width.

### -param pcyHeight [out]

Type: <b>long*</b>

Address, in pixels, of the variable that receives the object's height.

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the location that the server returns should be that of the object or that of one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK. Clients must always check that output parameters contain valid values.

If not successful, returns one of the values in the table that follows, or another standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>. For more information, see <a href="/windows/desktop/WinAuto/checking-iaccessible-return-values">Checking IAccessible Return Values</a>.

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

This method retrieves the object's bounding rectangle. If the object has a non-rectangular shape, then this method returns the smallest rectangle that completely encompasses the entire object region. For non-rectangular objects, the coordinates of the object's bounding rectangle could fail if tested with <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-acchittest">IAccessible::accHitTest</a>. Examples of such non-rectangular objects are list view items in large-icon mode where a single item has a rectangle for the icon and another rectangle for the text of the icon. Because <b>accLocation</b> returns a bounding rectangle, not all points in that rectangle will be within the actual bounds of the object. Some points within the bounding rectangle may not be on the object. For more information, see <a href="/windows/desktop/WinAuto/navigation-through-hit-testing-and-screen-location">Navigation Through Hit Testing and Screen Location</a>.

<b>Note:  </b>This method returns width and height. If you want the right and bottom coordinates, calculate them using right = left + width, and bottom = top + height.



<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example shows a possible implementation of the method for a custom list box whose list items are child elements. For the list box itself, the call is passed to the standard accessible object, which returns the screen coordinates of the window.


```cpp

// m_pStdAccessibleObject is the standard accessible object for the control window. 
// m_pControl is the object that represents the control. Its GetItemRect method  
//   retrieves the screen coordinates of the specified item in a zero-based collection. 
// 
HRESULT STDMETHODCALLTYPE AccServer::accLocation( 
    long *pxLeft,
    long *pyTop,
    long *pcxWidth,
    long *pcyHeight,
    VARIANT varChild)
{
    *pxLeft = 0;
    *pyTop = 0;
    *pcxWidth = 0;
    *pcyHeight = 0;
    if (varChild.vt != VT_I4)
    {
        return E_INVALIDARG;
    }
    if (varChild.lVal == CHILDID_SELF)
    {
        return m_pStdAccessibleObject->accLocation(pxLeft, pyTop, pcxWidth, pcyHeight, varChild);
    }
    else
    {
        RECT rect;
        if (m_pControl->GetItemRect(varChild.lVal - 1, &rect) == FALSE)
        {
            return E_INVALIDARG;
        }
        else
        {
            *pxLeft = rect.left;
            *pyTop = rect.top;
            *pcxWidth = rect.right - rect.left;
            *pcyHeight = rect.bottom - rect.top;
            return S_OK;        
        }
    }
};

```

## -see-also

<a href="/windows/desktop/WinAuto/active-accessibility-and-windows-vista-screen-scaling">Active Accessibility and Windows Vista Screen Scaling</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-acchittest">IAccessible::accHitTest</a>



<a href="/windows/desktop/WinAuto/navigation-through-hit-testing-and-screen-location">Navigation Through Hit Testing and Screen Location</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>