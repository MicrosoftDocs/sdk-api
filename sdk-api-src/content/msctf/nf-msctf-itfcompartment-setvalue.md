---
UID: NF:msctf.ITfCompartment.SetValue
title: ITfCompartment::SetValue
author: windows-sdk-content
description: ITfCompartment::SetValue method
old-location: tsf\itfcompartment_setvalue.htm
old-project: TSF
ms.assetid: 1a1a175f-a24e-4f83-92d3-ac6a24f5f486
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfCompartment interface [Text Services Framework],SetValue method, ITfCompartment.SetValue, ITfCompartment::SetValue, SetValue, SetValue method [Text Services Framework], SetValue method [Text Services Framework],ITfCompartment interface, _tsf_itfcompartment_setvalue_ref, msctf/ITfCompartment::SetValue, tsf.itfcompartment_setvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfCompartment.SetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCompartment::SetValue


## -description




## -parameters




### -param tid [in]

Contains a <a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId</a> value that identifies the client.


### -param pvarValue [in]

Pointer to a VARIANT structure that contains the data to be set. Only VT_I4, VT_UNKNOWN and VT_BSTR data types are allowed.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pvarValue</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The compartment was cleared by a call to <a href="https://msdn.microsoft.com/862ec077-b192-412a-b80c-6105f503ed21">ITfCompartmentMgr::ClearCompartment</a>, this method was called during a <a href="https://msdn.microsoft.com/1756754c-6353-4296-bdb5-1cbef1d29ec5">ITfCompartmentEventSink::OnChange</a> notification or only the owner can clear this compartment.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3">ITfCompartment</a>



<a href="https://msdn.microsoft.com/984dc390-6e15-4491-8c06-77c27c5bdd6f">TfClientId
      </a>
 

 

