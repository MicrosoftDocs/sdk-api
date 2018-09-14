---
UID: NF:oleauto.SafeArrayDestroy
title: SafeArrayDestroy function
author: windows-sdk-content
description: Destroys an existing array descriptor and all of the data in the array.
old-location: automat\safearraydestroy.htm
tech.root: automat
ms.assetid: fc94f7e7-b903-4c78-905c-54df1f8d13fa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SafeArrayDestroy, SafeArrayDestroy function [Automation], _oa96_SafeArrayDestroy, automat.safearraydestroy, oleauto/SafeArrayDestroy
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
 - SafeArrayDestroy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayDestroy function


## -description


Destroys an existing array descriptor and all of the data in the array. If objects are stored in the array, <b>Release</b> is called on each object in the array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.


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
<dt><b>DISP_E_ARRAYISLOCKED</b></dt>
</dl>
</td>
<td width="60%">
The array is locked.

</td>
</tr>
</table>
 




## -remarks



Safe arrays of variant will have the <a href="https://msdn.microsoft.com/28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a> function called on each member and safe arrays of BSTR will have the <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function called on each element. <a href="https://msdn.microsoft.com/979b0702-3342-4036-8113-c84728436ab6">IRecordInfo::RecordClear</a> will be called to release object references and other values of a record without deallocating the record.



#### Examples


```cpp
STDMETHODIMP_(ULONG) CEnumPoint::Release()
{
   if(--m_refs == 0){
      if(m_psa != NULL)
      SafeArrayDestroy(m_psa);
      delete this;
      return 0;
   }
   return m_refs;
}
```




