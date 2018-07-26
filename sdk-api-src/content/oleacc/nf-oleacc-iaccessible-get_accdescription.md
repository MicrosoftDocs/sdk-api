---
UID: NF:oleacc.IAccessible.get_accDescription
title: IAccessible::get_accDescription
author: windows-sdk-content
description: The IAccessible::get_accDescription method retrieves a string that describes the visual appearance of the specified object. Not all objects have a description.
old-location: winauto\iaccessible_iaccessible__get_accdescription.htm
old-project: WinAuto
ms.assetid: ca70c5bc-ac20-41fe-a9fe-f4a7209c5958
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accDescription method, IAccessible.get_accDescription, IAccessible::get_accDescription, _msaa_IAccessible_get_accDescription, get_accDescription, get_accDescription method [Windows Accessibility], get_accDescription method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accdescription, oleacc/IAccessible::get_accDescription, winauto.iaccessible_iaccessible__get_accdescription
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: QACONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessible.get_accDescription
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: ADAM
---

# IAccessible::get_accDescription


## -description


The <b>IAccessible::get_accDescription</b> method retrieves a string that describes the visual appearance of the specified object. Not all objects have a description.
<div class="alert"><b>Note</b>  The Description property is often used incorrectly and is not supported by Microsoft UI Automation. Microsoft Active Accessibility server developers should not use this property. If more information is needed for accessibility and automation scenarios, use the 
properties supported by UI Automation elements and control patterns.</div><div> </div>

## -parameters




### -param varChild




### -param pszDescription [out, retval]

Type: <b>BSTR*</b>

 Address of a <b>BSTR</b> that receives a localized string that describes the specified object, or <b>NULL</b> if this object has no description.


#### - varID [in]

Type: <b>VARIANT</b>

Specifies whether the retrieved description belongs to the object or one of the object's child elements. This parameter is either CHILDID_SELF (to obtain information about the object) or a child ID (to obtain information about the object's child element). For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>. Servers return these values, but clients must always check output parameters to ensure that they contain valid values. For more information, see <a href="https://msdn.microsoft.com/0def0349-178b-4be5-aa1d-6602dc015981">Checking IAccessible Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified object does not have a description.

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



An Microsoft Active Accessibility server can add support for UI Automation by using Direct Annotation, using the <a href="https://msdn.microsoft.com/90211503-a73c-4380-be96-0be40ad29382">IAccessibleEx</a> interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message.

This property provides a textual equivalent of the object for the user. The description should be similar to the text supplied with the ALT attribute in HTML, which is the text that is displayed to describe images for people using text-only browsers. However, some controls use this property to store extra information about the control that is not related to a textual equivalent. For more information about this property, see <a href="https://msdn.microsoft.com/1fe3221f-e1dd-44b2-b749-d00bee1b6b89">Description Property</a>.

<b>Note to server developers:  </b>
              Localize the string returned from this property.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows one possible implementation of this method for a custom list box that maintains its own child elements. The example demonstrates the syntax, but remember that a real text-only list box would probably not need to support this property. For simplicity, the strings in the example are not localized.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT STDMETHODCALLTYPE AccServer::get_accDescription( 
    VARIANT varChild,
    BSTR *pszDescription)
{
    if (varChild.vt != VT_I4)
    {
        *pszDescription = NULL;
        return E_INVALIDARG;
    }
    if (varChild.lVal == CHILDID_SELF)
    {
        *pszDescription = SysAllocString(L"List of contacts.");    
            
    }
    else
    {
        *pszDescription = SysAllocString(L"A contact.");           
            
    }
    return S_OK;
};
</pre>
</td>
</tr>
</table></span></div>
<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function retrieves the description of the specified accessible object, or a child element, and displays it on the console.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT PrintDescription(IAccessible* pAcc, long child)
{
    VARIANT varObject;
    varObject.vt = VT_I4;
    varObject.lVal = child;
    BSTR bstrDesc;
    HRESULT hr = pAcc-&gt;get_accDescription(varObject, &amp;bstrDesc);
    if (hr == S_OK)
    {
        printf("Description: %S\n", bstrDesc);
        SysFreeString(bstrDesc);
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/1fe3221f-e1dd-44b2-b749-d00bee1b6b89">Description Property</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/ef541ef9-ae9f-4a8c-8dd1-f221eddb55c7">IAccessible::get_accHelp</a>



<a href="https://msdn.microsoft.com/344e95e1-45a5-4951-b545-1a938bfc8a8c">IAccessible::get_accName</a>



<a href="https://msdn.microsoft.com/8e29adec-13fb-4a85-87ac-9e8034dce147">IAccessible::get_accValue</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/d9d78e74-dcab-4974-945f-e8c5d42c04b7">Using Direct Annotation</a>
 

 

