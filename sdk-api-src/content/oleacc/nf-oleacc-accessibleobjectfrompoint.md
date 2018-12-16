---
UID: NF:oleacc.AccessibleObjectFromPoint
title: AccessibleObjectFromPoint function
author: windows-sdk-content
description: Retrieves the address of the IAccessible interface pointer for the object displayed at a specified point on the screen.
old-location: winauto\accessibleobjectfrompoint.htm
tech.root: WinAuto
ms.assetid: b781b74f-5c36-4a65-a9b1-ecf7f8e5b531
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AccessibleObjectFromPoint, AccessibleObjectFromPoint function [Windows Accessibility], _msaa_AccessibleObjectFromPoint, msaa.accessibleobjectfrompoint, oleacc/AccessibleObjectFromPoint, winauto.accessibleobjectfrompoint
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - AccessibleObjectFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
---

# AccessibleObjectFromPoint function


## -description


Retrieves the address of the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface pointer for the object displayed at a specified point on the screen.


## -parameters




### -param ptScreen [in]

Specifies, in physical screen coordinates, the point that is examined.


### -param ppacc [out]

Address of a pointer variable that receives the address of the object's <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface.


### -param pvarChild [out]

Address of a <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a> structure that specifies whether the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface pointer that is returned in <i>ppacc</i> belongs to the object displayed at the specified point, or to the parent of the element at the specified point. The <b>vt</b> member of the <b>VARIANT</b> is always VT_I4. If the <b>lVal</b> member is CHILDID_SELF, then the <b>IAccessible</b> interface pointer at <i>ppacc</i> belongs to the object at the point. If the <b>lVal</b> member is not CHILDID_SELF, <i>ppacc</i> is the address of the <b>IAccessible</b> interface of the child element's parent object. Clients must call <a href="https://msdn.microsoft.com/en-us/library/ms221165(v=VS.85).aspx">VariantClear</a> on the retrieved <b>VARIANT</b> parameter when finished using it.


## -returns



If successful, returns S_OK.

If not successful, returns one of the following or another standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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



This function retrieves the lowest-level accessible object in the object hierarchy at a given point. If the element at the point is not an accessible object (that is, does not support <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>), then the function retrieves the <b>IAccessible</b> interface of the parent object. The parent object must provide information about the child element through the <b>IAccessible</b> interface. Call <a href="https://msdn.microsoft.com/87327086-a8f3-4d1c-ab4d-8f5aba00c61a">IAccessible::accHitTest</a> to identify the child element at the specified screen coordinates.

As with other <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> methods and functions, clients might receive errors for <b>IAccessible</b> interface pointers because of a user action. For more information, see <a href="https://msdn.microsoft.com/408bfa47-fda0-4a25-89c1-da41d967ad61">Receiving Errors for IAccessible Interface Pointers</a>.

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




<a href="https://msdn.microsoft.com/d453c163-3918-4a1c-9636-16816227a295">AccessibleObjectFromEvent</a>



<a href="https://msdn.microsoft.com/297ac50f-2a58-477b-ba57-5d1416c191b3">AccessibleObjectFromWindow</a>



<a href="https://msdn.microsoft.com/c781fefd-09f0-4340-b3d3-f4e57308f392">Active Accessibility and Windows Vista Screen Scaling</a>



<a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>



<a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT Structure</a>
 

 

