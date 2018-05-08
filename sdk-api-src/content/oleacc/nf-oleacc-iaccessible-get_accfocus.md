---
UID: NF:oleacc.IAccessible.get_accFocus
title: IAccessible::get_accFocus
author: windows-driver-content
description: The IAccessible::get_accFocus method retrieves the object that has the keyboard focus. All objects that may receive the keyboard focus must support this property.
old-location: winauto\iaccessible_iaccessible__get_accfocus.htm
old-project: WinAuto
ms.assetid: 42114c5d-8f28-458a-8d22-ac1531cd50d2
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accFocus method, IAccessible.get_accFocus, IAccessible::get_accFocus, VT_DISPATCH, VT_EMPTY, VT_I4, _msaa_IAccessible_get_accFocus, get_accFocus, get_accFocus method [Windows Accessibility], get_accFocus method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accfocus, oleacc/IAccessible::get_accFocus, winauto.iaccessible_iaccessible__get_accfocus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Oleacc.dll
api_name:
-	IAccessible.get_accFocus
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IAccessible::get_accFocus


## -description


The <b>IAccessible::get_accFocus</b> method retrieves the object that has the keyboard focus. All objects that may receive the keyboard focus must support this property.


## -parameters




### -param pvarChild






#### - pvarID [out, retval]

Type: <b>VARIANT*</b>

Address of a <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT structure</a> that receives information about the object that has the focus. The following table describes the information returned in <i>pvarID</i>.

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
<b>pdispVal</b> member is the address of the <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch interface</a> for the child object that has the keyboard focus.

</td>
</tr>
</table>
 


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
The object is a window but not not the foreground window.

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

Only one object or item within a container has the focus at any one time. The object with the keyboard focus is not always the selected object. For more information about the difference between selection and focus, see <a href="https://msdn.microsoft.com/8170fe19-f157-4d7d-8eec-d384e51f1560">Selection and Focus Properties and Methods</a>.

This method returns either an <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface pointer or a child ID for the <i>pvarID</i>. For more information about how to use the <b>IDispatch</b> interface pointer or child ID, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.

As with other <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="https://msdn.microsoft.com/408bfa47-fda0-4a25-89c1-da41d967ad61">Receiving Errors for IAccessible Interface Pointers</a>.

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows a possible implementation of this method for a custom single-selection list box. If the control does not have the focus, VT_EMPTY is returned in the variant by the standard accessible object for the HWND. If the control does have the focus, and an item is selected, the child ID of that item is returned; if there is no selection, CHILDID_SELF is returned.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// m_pControl is the control object that is served by this implementation. 
// m_pStdAccessibleObject is the object returned by CreateStdAccessibleObject. 

HRESULT STDMETHODCALLTYPE AccServer::get_accFocus(VARIANT *pvarChild)
{
    FAIL_IF_NO_CONTROL;  // Macro that checks for existence of control. 

    HRESULT hr = m_pStdAccessibleObject-&gt;get_accFocus(pvarChild);  
    if (pvarChild-&gt;vt != VT_I4)
    {
        return hr;
    }
    else
    {
        int index = m_pControl-&gt;GetSelectedIndex();
        if (index &lt;0)
        {
            pvarChild-&gt;lVal = CHILDID_SELF;
        }
        else
        {
            // Convert to 1-based index for child ID. 
            pvarChild-&gt;lVal = index + 1;
        }
    }
    return S_OK;
};

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/ae55831c-0dfa-4901-b241-27e2cdf1035f">IAccessible::accSelect</a>



<a href="https://msdn.microsoft.com/80df32de-a99f-4a5a-b354-f3e133f3e620">IAccessible::get_accSelection</a>



<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>



<a href="https://msdn.microsoft.com/8170fe19-f157-4d7d-8eec-d384e51f1560">Selection and Focus Properties and Methods</a>
 

 

