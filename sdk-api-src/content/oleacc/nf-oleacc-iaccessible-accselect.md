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

# IAccessible::accSelect


## -description


The <b>IAccessible::accSelect</b> method modifies the selection or moves the keyboard focus of the specified object. All objects that support selection or receive the keyboard focus must support this method.


## -parameters




### -param flagsSelect [in]

Type: <b>long</b>

Specifies which selection or focus operations are to be performed. This parameter must have a combination of the <a href="https://msdn.microsoft.com/52755540-dcf4-4e0b-bb5c-88b05f134d79">SELFLAG Constants</a>.


### -param varChild






#### - varID [in]

Type: <b>VARIANT</b>

Specifies the selected object. If the value is CHILDID_SELF, the object itself is selected; if a child ID, one of the object's child elements is selected. For more information about initializing the <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns one of the values in the table that follows, or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.

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
An argument is not valid. This return value means that the specified SELFLAG combination is not valid, or that the SELFLAG value does not make sense for the specified object. For example, the following flags are not allowed on a single-selection list box: <a href="selflag.htm">SELFLAG_EXTENDSELECTION</a>, <a href="selflag.htm">SELFLAG_ADDSELECTION</a>, and <a href="selflag.htm">SELFLAG_REMOVESELECTION</a>.

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



Client applications use this method to perform complex selection operations. For more information, see <a href="https://msdn.microsoft.com/5e7ad1e9-b1b2-4e76-93e8-b58251930621">Selecting Child Objects</a>. This method provides the simplest way to programmatically switch the input focus between applications. This applies to applications running on Windows 2000.

<b>Note:  </b>
              This method is for the selection of items, not text.
            

<h3><a id="Client_Example"></a><a id="client_example"></a><a id="CLIENT_EXAMPLE"></a>Client Example</h3>
The following example function selects the item at a specified point on the screen. It is assumed that a single selection is wanted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT SelectItemAtPoint(POINT point)
{
    VARIANT varItem;
    IAccessible* pAcc;
    HRESULT hr = AccessibleObjectFromPoint(point, &amp;pAcc, &amp;varItem);
    if ((hr == S_OK))
    {
        hr = pAcc-&gt;accSelect((SELFLAG_TAKEFOCUS | SELFLAG_TAKESELECTION), varItem);
        VariantClear(&amp;varItem);
        pAcc-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/42114c5d-8f28-458a-8d22-ac1531cd50d2">IAccessible::get_accFocus</a>



<a href="https://msdn.microsoft.com/80df32de-a99f-4a5a-b354-f3e133f3e620">IAccessible::get_accSelection</a>



<a href="https://msdn.microsoft.com/52755540-dcf4-4e0b-bb5c-88b05f134d79">SELFLAG</a>



<a href="https://msdn.microsoft.com/8170fe19-f157-4d7d-8eec-d384e51f1560">Selection and Focus Properties and Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

