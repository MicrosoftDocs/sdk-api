---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAccessible::get_accName


## -description


The <b>IAccessible::get_accName</b> method retrieves the name of the specified object. All objects support this property.


## -parameters




### -param varChild




### -param pszName [out, retval]

Type: <b>BSTR*</b>

Address of a <b>BSTR</b> that receives a string that contains the specified object's name.


#### - varID [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved name belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="https://msdn.microsoft.com/0def0349-178b-4be5-aa1d-6602dc015981">Checking IAccessible Return Values</a>.

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



Many objects such as icons, menus, check boxes, combo boxes, and other controls have labels that are displayed to users. Any label that is displayed to users is used for the object's name property. For more information, see the <a href="https://msdn.microsoft.com/7533955a-9538-4ead-a6ca-f61dd1b4d5c5">Name Property</a>.

<b>Note to server developers:  </b>If you are using menu or button text for the Name property, remove any ampersands (&amp;) marking the keyboard access keys. Provide the access key to the client in response to <a href="https://msdn.microsoft.com/0d91c791-1e9b-45da-8fa6-b879ac6d11a7">IAccessible::get_accKeyboardShortcut</a>.

Localize the string returned from this property.



<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example shows a possible implementation of this method for a custom list box control that manages its own child elements.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
        return m_pStdAccessibleObject-&gt;get_accName(varChild, pszName);                  
    }
    
    // Else return the name of the item in the list. 
    else
    {
        CustomListControlItem* pItem = m_pControl-&gt;GetItemAt(varChild.lVal - 1);
        if (pItem)
        {
            *pszName = SysAllocString(pItem-&gt;GetName());        
       
        }
    }
    return S_OK;
};
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function displays the accessible name of a control.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
    HRESULT hr = pAcc-&gt;get_accName(varChild, &amp;bstrName);
    printf("Name: %S ", bstrName);
    SysFreeString(bstrName);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/0d91c791-1e9b-45da-8fa6-b879ac6d11a7">IAccessible::get_accKeyboardShortcut</a>



<a href="https://msdn.microsoft.com/7533955a-9538-4ead-a6ca-f61dd1b4d5c5">Name Property</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

