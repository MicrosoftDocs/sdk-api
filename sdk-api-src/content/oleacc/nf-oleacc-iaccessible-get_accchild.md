---
UID: NF:oleacc.IAccessible.get_accChild
title: IAccessible::get_accChild (oleacc.h)
description: The IAccessible::get_accChild method retrieves an IDispatch for the specified child, if one exists. All objects must support this property.
helpviewer_keywords: ["IAccessible interface [Windows Accessibility]","get_accChild method","IAccessible.get_accChild","IAccessible::get_accChild","_msaa_IAccessible_get_accChild","get_accChild","get_accChild method [Windows Accessibility]","get_accChild method [Windows Accessibility]","IAccessible interface","msaa.iaccessible_iaccessible__get_accchild","oleacc/IAccessible::get_accChild","winauto.iaccessible_iaccessible__get_accchild"]
old-location: winauto\iaccessible_iaccessible__get_accchild.htm
tech.root: WinAuto
ms.assetid: 64b0c24d-778a-4f13-8c70-6be3436a98cd
ms.date: 12/05/2018
ms.keywords: IAccessible interface [Windows Accessibility],get_accChild method, IAccessible.get_accChild, IAccessible::get_accChild, _msaa_IAccessible_get_accChild, get_accChild, get_accChild method [Windows Accessibility], get_accChild method [Windows Accessibility],IAccessible interface, msaa.iaccessible_iaccessible__get_accchild, oleacc/IAccessible::get_accChild, winauto.iaccessible_iaccessible__get_accchild
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
 - IAccessible::get_accChild
 - oleacc/IAccessible::get_accChild
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
 - IAccessible.get_accChild
---

# IAccessible::get_accChild


## -description

The <b>IAccessible::get_accChild</b> method retrieves an <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> for the specified child, if one exists. All objects must support this property.

## -parameters

### -param varChild [in]

Type: <b>VARIANT</b>

Identifies the child whose <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface is retrieved. For more information about initializing the <a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>, see <a href="/windows/desktop/WinAuto/how-child-ids-are-used-in-parameters">How Child IDs Are Used in Parameters</a>.

### -param ppdispChild [out, retval]

Type: <b>IDispatch**</b>

[out, retval] Receives the address of the child object's <a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface.

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

Servers expose elements as either elements (child IDs) or full objects (<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface pointers). If a child is an element, <b>get_accChild</b> returns S_FALSE, and the parent will provide information for that child. If the child is a full object, <b>get_accChild</b> will return the <b>IAccessible</b> interface pointer and the parent will not provide information about that child. If <b>get_accChild</b> fails because the server application cannot create an accessible object due to a temporary system error (such as an out-of-memory error), the server should return a suitable failure code.

<b>Note to server developers:  </b>If <i>varChildID</i> contains VT_EMPTY, you should return E_INVALIDARG.
            

<h3><a id="Server_Example"></a><a id="server_example"></a><a id="SERVER_EXAMPLE"></a>Server Example</h3>
The following example code shows an implementation for an object that does not have any children, or whose children are elements rather than objects.


```cpp

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

```

## -see-also

<a href="/windows/desktop/api/oleacc/nf-oleacc-accessiblechildren">AccessibleChildren</a>



<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>



<a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accparent">IAccessible::get_accParent</a>



<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a>



<a href="/windows/desktop/WinAuto/object-navigation-properties-and-methods">Object Navigation Properties and Methods</a>



<a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>