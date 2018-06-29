---
UID: NF:oleauto.SafeArrayCreateEx
title: SafeArrayCreateEx function
author: windows-sdk-content
description: Creates and returns a safe array descriptor from the specified VARTYPE, number of dimensions and bounds.
old-location: automat\safearraycreateex.htm
old-project: automat
ms.assetid: 63117428-6676-4fb5-a0ae-7e3b22546d77
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: SafeArrayCreateEx, SafeArrayCreateEx function [Automation], _oa96_SafeArrayCreateEx, automat.safearraycreateex, oleauto/SafeArrayCreateEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayCreateEx
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SafeArrayCreateEx function


## -description


Creates and returns a safe array descriptor from the specified VARTYPE, number of dimensions and bounds.


## -parameters




### -param vt [in]

The base type or the VARTYPE of each element of the array. The FADF_RECORD flag can be set for a variant type VT_RECORD, The FADF_HAVEIID flag can be set for VT_DISPATCH or VT_UNKNOWN, and FADF_HAVEVARTYPE can be set for all other VARTYPEs.


### -param cDims [in]

The number of dimensions in the array.




### -param rgsabound [in]

A vector of bounds (one for each dimension) to allocate for the array.



### -param pvExtra [in]

the type information of the user-defined type, if you are creating a safe array of user-defined types. If the vt parameter is VT_RECORD, then <i>pvExtra</i> will be a pointer to an <a href="https://msdn.microsoft.com/065ebfa8-bfac-4c75-a3f9-9dc0409ea454">IRecordInfo</a> describing the record. If the <i>vt</i> parameter is VT_DISPATCH or VT_UNKNOWN, then <i>pvExtra</i> will contain a pointer to a GUID representing the type of interface being passed to the array.


## -returns



A safe array descriptor, or null if the array could not be created.




## -remarks



If the VARTYPE is VT_RECORD then <a href="https://msdn.microsoft.com/85317e8e-7625-4799-9c34-73245f164f85">SafeArraySetRecordInfo</a> is called. If the VARTYPE is VT_DISPATCH or VT_UNKNOWN then the elements of the array must contain interfaces of the same type. Part of the process of marshaling this array to other processes does include generating the proxy/stub code of the IID pointed to by the <i>pvExtra</i> parameter. To actually pass heterogeneous interfaces one will need to specify either IID_IUnknown or IID_IDispatch in <i>pvExtra</i> and provide some other means for the caller to identify how to query for the actual interface.


#### Examples

The following example describes how a safe array of user-defined types is stored into a variant of type VT_RECORD.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SAFEARRAYBOUND * sab;
sab.cElements = 2;
sab.lLbound = 0;
hresult hr;

SAFEARRAY Sa;
Sa = SafeArrayCreateEx(VT_RECORD, 1, &amp;sab, pRecInfo);
if (Sa == NULL)
   return E_OUTOFMEMORY;

PVOID pvData;
hr = SafeArrayAccessData(Sa, &amp;pvData);
if (FAILED(hr)) {
   SafeArrayDestroy(Sa);
   return hr;
}

TEST * pTest;
pTest = (TEST *)pvData;
pTest[0] = a;
pTest[1] = b;
hr = SafeArrayUnaccessData(Sa);
if (FAILED(hr)) {
   SafeArrayDestroy(Sa);
   return hr;
}

VariantInit(&amp;variant);
V_VT(&amp;variant) = VT_ARRAY|VT_RECORD;
V_ARRAY(&amp;variant) = Sa;</pre>
</td>
</tr>
</table></span></div>


