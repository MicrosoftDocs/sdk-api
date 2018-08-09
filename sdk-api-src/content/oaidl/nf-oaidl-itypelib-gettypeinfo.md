---
UID: NF:oaidl.ITypeLib.GetTypeInfo
title: ITypeLib::GetTypeInfo
author: windows-sdk-content
description: Retrieves the specified type description in the library.
old-location: automat\itypelib_gettypeinfo.htm
old-project: automat
ms.assetid: 7661faa8-eb06-4bbe-88e9-9662a0d6984b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTypeInfo, GetTypeInfo method [Automation], GetTypeInfo method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetTypeInfo method, ITypeLib.GetTypeInfo, ITypeLib::GetTypeInfo, _oa96_ITypeLib_GetTypeInfo, automat.itypelib_gettypeinfo, oaidl/ITypeLib::GetTypeInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeLib.GetTypeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITypeLib::GetTypeInfo


## -description


Retrieves the specified type description in the library.


## -parameters




### -param index [in]

The index of the interface to be returned.




### -param ppTInfo [out]

If successful, returns a pointer to the pointer to the <a href="https://msdn.microsoft.com/f3356463-3373-4279-bae1-953378aa2680">ITypeInfo</a> interface.



## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is outside the range of  to <a href="https://msdn.microsoft.com/63436bee-c71b-4d32-bfca-426c8953a75b">GetTypeInfoCount</a> - 1.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



For dual interfaces, <b>GetTypeInfo</b>returns only the TKIND_DISPATCH type information. To get the TKIND_INTERFACE type information, <a href="https://msdn.microsoft.com/aec61a9a-fa4f-42cd-a74b-100cdf2c2624">GetRefTypeOfImplType</a> can be called on the TKIND_DISPATCH type information, passing an index of –1. Then, the returned type information handle can be passed to <a href="https://msdn.microsoft.com/61d3b31d-6591-4e55-9e82-5246a168be00">GetRefTypeInfo</a>.


#### Examples

The following example gets the TKIND_INTERFACE type information for a dual interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
hr = ptlib-&gt;GetTypeInfo((unsigned int) dwIndex, &amp;ptypeinfoDisp);
if (FAILED(hr)) {
   //free resources
   return hr;
}
hr = ptypeinfoDisp-&gt;GetRefTypeOfImplType(-1, &amp;phreftype);
if (FAILED(hr)) {
   //free resources
   return hr;

hr = ptypeinfoDisp-&gt;GetRefTypeInfo(phreftype, &amp;ptypeinfoInt);
if (FAILED(hr)) {
   //free resources
   return hr;

// </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c1e5d71f-6a4e-45f3-811d-f57024f81a55">ITypeLib</a>
 

 

