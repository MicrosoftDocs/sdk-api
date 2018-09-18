---
UID: NF:oleauto.SafeArrayAccessData
title: SafeArrayAccessData function
author: windows-sdk-content
description: Increments the lock count of an array, and retrieves a pointer to the array data.
old-location: automat\safearrayaccessdata.htm
tech.root: automat
ms.assetid: ded2112e-f6cd-4982-bacb-b95370e80187
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SafeArrayAccessData, SafeArrayAccessData function [Automation], _oa96_SafeArrayAccessData, automat.safearrayaccessdata, oleauto/SafeArrayAccessData
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayAccessData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayAccessData function


## -description


Increments the lock count of an array, and retrieves a pointer to the array data.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


### -param ppvData [out]

The array data.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The array could not be locked.

</td>
</tr>
</table>
 




## -remarks



After calling <b>SafeArrayAccessData</b>, you must call the <a href="https://msdn.microsoft.com/61b482cb-f0a3-4efb-9a68-f373f241e89a">SafeArrayUnaccessData</a> function to unlock the array.


#### Examples

The following example sorts a safe array of one dimension that contains BSTRs by accessing the array elements directly. This approach is faster than using <a href="https://msdn.microsoft.com/47e9ee31-1e3b-4193-8467-6ef0db05966e">SafeArrayGetElement</a> and <a href="https://msdn.microsoft.com/7c837b4f-d319-4d98-934a-b585fe521bf8">SafeArrayPutElement</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>long i, j, min; 
BSTR bstrTemp;
BSTR HUGEP *pbstr;
HRESULT hr;

// Get a pointer to the elements of the array.
hr = SafeArrayAccessData(psa, (void HUGEP**)&amp;pbstr);
if (FAILED(hr))
goto error;

// Selection sort.
for (i = 0; i &lt; psa-&gt;rgsabound.cElements-1; i++)
{
   min = i;
   for (j = i+1; j &lt; psa-&gt;rgsabound.cElements; j++)
   {
      if (wcscmp(pbstr[j], pbstr[min]) &lt; 0)
         min = j; 
   }

   // Swap array[min] and array[i].
   bstrTemp = pbstr[min];
   pbstr[min] = pbstr[i];
   pbstr[i] = bstrTemp;

}

SafeArrayUnaccessData(psa);</pre>
</td>
</tr>
</table></span></div>


