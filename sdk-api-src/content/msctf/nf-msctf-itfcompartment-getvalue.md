---
UID: NF:msctf.ITfCompartment.GetValue
title: ITfCompartment::GetValue
author: windows-driver-content
description: ITfCompartment::GetValue method
old-location: tsf\itfcompartment_getvalue.htm
old-project: TSF
ms.assetid: 31a9efbd-ebde-4877-a387-ebaccd97d732
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetValue, GetValue method [Text Services Framework], GetValue method [Text Services Framework],ITfCompartment interface, ITfCompartment interface [Text Services Framework],GetValue method, ITfCompartment.GetValue, ITfCompartment::GetValue, _tsf_itfcompartment_getvalue_ref, msctf/ITfCompartment::GetValue, tsf.itfcompartment_getvalue
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfCompartment.GetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCompartment::GetValue


## -description




## -parameters




### -param pvarValue [out]

Pointer to a <b>VARIANT</b> structure that receives the data. This receives VT_EMPTY if the compartment has no value. The caller must free this data when it is no longer required by calling <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The compartment has no value. <i>pvarValue</i> receives VT_EMPTY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The compartment has been cleared by a call to <a href="https://msdn.microsoft.com/862ec077-b192-412a-b80c-6105f503ed21">ITfCompartmentMgr::ClearCompartment</a>.

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
</table>
 




## -remarks



The caller must recognize the supplied data format in order to use the data. The compartment installer must publish the data format to enable other clients to use it.




## -see-also




<a href="https://msdn.microsoft.com/c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3">ITfCompartment</a>



<a href="https://msdn.microsoft.com/862ec077-b192-412a-b80c-6105f503ed21">ITfCompartmentMgr::ClearCompartment
      </a>



<a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>
 

 

