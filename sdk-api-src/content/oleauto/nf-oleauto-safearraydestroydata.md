---
UID: NF:oleauto.SafeArrayDestroyData
title: SafeArrayDestroyData function
author: windows-sdk-content
description: Destroys all the data in the specified safe array.
old-location: automat\safearraydestroydata.htm
tech.root: automat
ms.assetid: aa9c62ba-79b5-4fcf-b3ed-664016486dfc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SafeArrayDestroyData, SafeArrayDestroyData function [Automation], _oa96_SafeArrayDestroyData, automat.safearraydestroydata, oleauto/SafeArrayDestroyData
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
 - SafeArrayDestroyData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayDestroyData function


## -description


Destroys all the data in the specified safe array. 


## -parameters




### -param psa [in]

A safe array descriptor.


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
The argument <i>psa</i> was not valid.

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



This function is typically used when freeing safe arrays that contain elements with data types other than variants. If objects are stored in the array, Release is called on each object in the array. Safe arrays of variant will have the <a href="https://msdn.microsoft.com/28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a> function called on each member and safe arrays of BSTR will have the <a href="https://msdn.microsoft.com/8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function called on each element. <a href="https://msdn.microsoft.com/979b0702-3342-4036-8113-c84728436ab6">IRecordInfo::RecordClear</a> will be called to release object references and other values of a record without deallocating the record.




