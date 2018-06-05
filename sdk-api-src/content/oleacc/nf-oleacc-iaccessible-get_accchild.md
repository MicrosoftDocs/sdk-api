---
UID: NF:oleacc.IAccessible.get_accChild
title: IAccessible::get_accChild
author: windows-sdk-content
description: The IAccessible::get_accChild method retrieves an IDispatch for the specified child, if one exists. All objects must support this property.
old-location: winauto\iaccessible_iaccessible__get_accchild.htm
old-project: WinAuto
ms.assetid: 64b0c24d-778a-4f13-8c70-6be3436a98cd
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accChild method, IAccessible.get_accChild, IAccessible::get_accChild, _msaa_IAccessible_get_accChild, get_accChild, get_accChild method [Windows Accessibility], get_accChild method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accchild, oleacc/IAccessible::get_accChild, winauto.iaccessible_iaccessible__get_accchild
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Oleacc.dll
api_name:
-	IAccessible.get_accChild
product: Windows
targetos: Windows
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAccessible::get_accChild


## -description


The <b>IAccessible::get_accChild</b> method retrieves an <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> for the specified child, if one exists. All objects must support this property.


## -parameters




### -param varChild




### -param ppdispChild [out, retval]

Type: <b>IDispatch**</b>

[out, retval] Receives the address of the child object's <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface.


#### - varChildID [in]

Type: <b>VARIANT</b>

Identifies the child whose <a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a> interface is retrieved. For more information about initializing the <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>, see <a href="https://msdn.microsoft.com/051ec5ba-540c-4ae1-b917-4c229557ca2f">How Child IDs Are Used in Parameters</a>.


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
The child is not an accessible object.

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



Servers expose elements as either elements (child IDs) or full objects (<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface pointers). If a child is an element, <b>get_accChild</b> returns S_FALSE, and the parent will provide information for that child. If the child is a full object, <b>get_accChild</b> will return the <b>IAccessible</b> interface pointer and the parent will not provide information about that child. If <b>get_accChild</b> fails because the server application cannot create an accessible object due to a temporary system error (such as an out-of-memory error), the server should return a suitable failure code.

<b>Note to server developers:  </b>
              If <i>varChildID</i> contains VT_EMPTY, you should return E_INVALIDARG.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows an implementation for an object that does not have any children, or whose children are elements rather than objects.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT STDMETHODCALLTYPE AccServer::get_accChild( 
    VARIANT varChild,
    IDispatch **ppdispChild)
{
    if (varChild.vt != VT_I4)
    {
        *ppdispChild = NULL;
        return E_INVALIDARG;
    }
    *ppdispChild = NULL;    
    return S_FALSE;     
};
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dc9262d8-f57f-41f8-8945-d95f38d197e9">AccessibleChildren</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/7c8c5208-ea77-47b2-913d-314ade0313f5">IAccessible::get_accParent</a>



<a href="https://msdn.microsoft.com/5a95f002-4fd5-43d3-9b50-7b3f7790300a">IDispatch</a>



<a href="https://msdn.microsoft.com/c6bcd044-bf70-4eec-92ae-66f9bd836c33">Object Navigation Properties and Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

