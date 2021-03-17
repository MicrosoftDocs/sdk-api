---
UID: NF:oleauto.SafeArrayAccessData
title: SafeArrayAccessData function (oleauto.h)
description: Increments the lock count of an array, and retrieves a pointer to the array data.
helpviewer_keywords: ["SafeArrayAccessData","SafeArrayAccessData function [Automation]","_oa96_SafeArrayAccessData","automat.safearrayaccessdata","oleauto/SafeArrayAccessData"]
old-location: automat\safearrayaccessdata.htm
tech.root: automat
ms.assetid: ded2112e-f6cd-4982-bacb-b95370e80187
ms.date: 12/05/2018
ms.keywords: SafeArrayAccessData, SafeArrayAccessData function [Automation], _oa96_SafeArrayAccessData, automat.safearrayaccessdata, oleauto/SafeArrayAccessData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayAccessData
 - oleauto/SafeArrayAccessData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayAccessData
---

# SafeArrayAccessData function


## -description

Increments the lock count of an array, and retrieves a pointer to the array data.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

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

After calling <b>SafeArrayAccessData</b>, you must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayunaccessdata">SafeArrayUnaccessData</a> function to unlock the array.


#### Examples

The following example sorts a safe array of one dimension that contains BSTRs by accessing the array elements directly. This approach is faster than using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement">SafeArrayGetElement</a> and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement">SafeArrayPutElement</a>.


```cpp
long i, j, min; 
BSTR bstrTemp;
BSTR HUGEP *pbstr;
HRESULT hr;

// Get a pointer to the elements of the array.
hr = SafeArrayAccessData(psa, (void HUGEP**)&pbstr);
if (FAILED(hr))
goto error;

// Selection sort.
for (i = 0; i < psa->rgsabound.cElements-1; i++)
{
   min = i;
   for (j = i+1; j < psa->rgsabound.cElements; j++)
   {
      if (wcscmp(pbstr[j], pbstr[min]) < 0)
         min = j; 
   }

   // Swap array[min] and array[i].
   bstrTemp = pbstr[min];
   pbstr[min] = pbstr[i];
   pbstr[i] = bstrTemp;

}

SafeArrayUnaccessData(psa);
```