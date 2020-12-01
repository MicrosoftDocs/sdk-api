---
UID: NF:oleacc.IAccessible.get_accName
title: IAccessible::get_accName (oleacc.h)
description: The IAccessible::get_accName method retrieves the name of the specified object. All objects support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accName method","IAccessible.get_accName","IAccessible::get_accName","_msaa_IAccessible_get_accName","get_accName","get_accName method [Windows Accessibility]","get_accName method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accname","oleacc/IAccessible::get_accName","winauto.iaccessible_iaccessible__get_accname"]
old-location: winauto\iaccessible_iaccessible__get_accname.htm
tech.root: WinAuto
ms.assetid: 344e95e1-45a5-4951-b545-1a938bfc8a8c
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accName method, IAccessible.get_accName, IAccessible::get_accName, _msaa_IAccessible_get_accName, get_accName, get_accName method [Windows Accessibility], get_accName method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accname, oleacc/IAccessible::get_accName, winauto.iaccessible_iaccessible__get_accname
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
 - IAccessible::get_accName
 - oleacc/IAccessible::get_accName
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
 - IAccessible.get_accName
---

# IAccessible::get_accName


## -description

The <b>IAccessible::get_accName</b> method retrieves the name of the specified object. All objects support this property.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved name belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT structure</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param pszName [out, retval]

Type: <b>BSTR*</b>

Address of a <b>BSTR</b> that receives a string that contains the specified object's name.

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
The specified object does not have a name.

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

Many objects such as icons, menus, check boxes, combo boxes, and other controls have labels that are displayed to users. Any label that is displayed to users is used for the object's name property. For more information, see the <a href="/windows/desktop/WinAuto/name-property">Name Property</a>.

<b>Note to server developers:  </b>If you are using menu or button text for the Name property, remove any ampersands (&amp;) marking the keyboard access keys. Provide the access key to the client in response to <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut">IAccessible::get_accKeyboardShortcut</a>.

Localize the string returned from this property.



<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example shows a possible implementation of this method for a custom list box control that manages its own child elements.


```cpp

// m_pStdAccessibleObject is the standard object returned by CreateStdAccessibleObject. 
// m_pControl is the control object that provides this accessibility object. It maintains
// a zero-based collection of child items. 

HRESULT STDMETHODCALLTYPE AccServer::get_accName( 
    VARIANT varChild,
    BSTR *pszName)
{
    if (varChild.vt != VT_I4)
    {
        *pszName = NULL;
        return E_INVALIDARG;
    }
    // For the control itself, let the standard accessible object return the name 
    // assigned by the application. This is either the "caption" property or, if 
    // there is no caption, the text of any label. 
    if (varChild.lVal == CHILDID_SELF)
    {
        return m_pStdAccessibleObject->get_accName(varChild, pszName);                  
    }
    
    // Else return the name of the item in the list. 
    else
    {
        CustomListControlItem* pItem = m_pControl->GetItemAt(varChild.lVal - 1);
        if (pItem)
        {
            *pszName = SysAllocString(pItem->GetName());        
       
        }
    }
    return S_OK;
};

```


<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function displays the accessible name of a control.


```cpp

HRESULT PrintName(IAccessible* pAcc, long childId)
{
    if (pAcc == NULL)
    {
        return E_INVALIDARG;
    }
    BSTR bstrName;
    VARIANT varChild;
    varChild.vt = VT_I4;
    varChild.lVal = childId;
    HRESULT hr = pAcc->get_accName(varChild, &bstrName);
    printf("Name: %S ", bstrName);
    SysFreeString(bstrName);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut">IAccessible::get_accKeyboardShortcut</a>



<a href="/windows/desktop/WinAuto/name-property">Name Property</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>