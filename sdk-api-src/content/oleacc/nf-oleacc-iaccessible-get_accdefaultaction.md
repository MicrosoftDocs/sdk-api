---
UID: NF:oleacc.IAccessible.get_accDefaultAction
title: IAccessible::get_accDefaultAction (oleacc.h)
description: The IAccessible::get_accDefaultAction method retrieves a string that indicates the object's default action. Not all objects have a default action.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accDefaultAction method","IAccessible.get_accDefaultAction","IAccessible::get_accDefaultAction","_msaa_IAccessible_get_accDefaultAction","get_accDefaultAction","get_accDefaultAction method [Windows Accessibility]","get_accDefaultAction method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accdefaultaction","oleacc/IAccessible::get_accDefaultAction","winauto.iaccessible_iaccessible__get_accdefaultaction"]
old-location: winauto\iaccessible_iaccessible__get_accdefaultaction.htm
tech.root: WinAuto
ms.assetid: 1261ff7c-7822-47c1-ac39-536b5ea09f31
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accDefaultAction method, IAccessible.get_accDefaultAction, IAccessible::get_accDefaultAction, _msaa_IAccessible_get_accDefaultAction, get_accDefaultAction, get_accDefaultAction method [Windows Accessibility], get_accDefaultAction method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accdefaultaction, oleacc/IAccessible::get_accDefaultAction, winauto.iaccessible_iaccessible__get_accdefaultaction
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
 - IAccessible::get_accDefaultAction
 - oleacc/IAccessible::get_accDefaultAction
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
 - IAccessible.get_accDefaultAction
---

# IAccessible::get_accDefaultAction


## -description

The <b>IAccessible::get_accDefaultAction</b> method retrieves a string that indicates the object's default action. Not all objects have a default action.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved default action is performed by the object or of one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pszDefaultAction [out, retval]

Type: <b>BSTR*</b>

Address of a <b>BSTR</b> that receives a localized string that describes the default action for the specified object; if this object has no default action, the value is <b>NULL</b>.

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
The specified object does not have a default action.

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
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_MEMBERNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified object does not support this property.

</td>
</tr>
</table>

## -remarks

The retrieved string describes the action that is performed on an object, not what the object does as a result. For example, a toolbar button that prints a document has a default action of "Press" rather than "Prints the current document."

Do not confuse an object's default action with its value. For more information, see <a href="/windows/desktop/WinAuto/defaultaction-property">DefaultAction Property</a>.

Only controls that perform actions support this method.

<b>Note to server developers:  </b>Localize the string returned from this property.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows a possible implementation of this method for a custom list box. For simplicity, the strings are not localized.


```cpp

HRESULT STDMETHODCALLTYPE AccServer::get_accDefaultAction( 
    VARIANT varChild,
    BSTR *pszDefaultAction)
{
    if (varChild.vt != VT_I4)
    {
        *pszDefaultAction = NULL;
        return E_INVALIDARG;
    }
    if (varChild.lVal == CHILDID_SELF)
    {
        *pszDefaultAction = SysAllocString(L"None.");
    }
    else
    {
        *pszDefaultAction = SysAllocString(L"Double-click");
    }
    return S_OK;
};

```

## -see-also

<a href="/windows/desktop/WinAuto/defaultaction-property">DefaultAction Property</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-accdodefaultaction">IAccessible::accDoDefaultAction</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>