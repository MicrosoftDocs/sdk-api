---
UID: NF:strmif.IBaseFilter.QueryVendorInfo
title: IBaseFilter::QueryVendorInfo method
author: windows-driver-content
description: The QueryVendorInfo method retrieves a string containing vendor information.
old-location: dshow\ibasefilter_queryvendorinfo.htm
old-project: DirectShow
ms.assetid: 7524de26-360e-49c7-b636-7d05cf4d0ad2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IBaseFilter, IBaseFilter interface [DirectShow], QueryVendorInfo method, IBaseFilter::QueryVendorInfo, IBaseFilterQueryVendorInfo, QueryVendorInfo method [DirectShow], QueryVendorInfo method [DirectShow], IBaseFilter interface, QueryVendorInfo,IBaseFilter.QueryVendorInfo, dshow.ibasefilter_queryvendorinfo, strmif/IBaseFilter::QueryVendorInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IBaseFilter.QueryVendorInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IBaseFilter::QueryVendorInfo method


## -description



The <code>QueryVendorInfo</code> method retrieves a string containing vendor information.




## -parameters




### -param pVendorInfo [out]

Address of a variable that receives a pointer to a wide-character string containing the vendor information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



This method is optional; filters are not required to support it.

If the method is supported, it uses the <b>CoTaskMemAlloc</b> function to allocate memory for the string. Call the <b>CoTaskMemFree</b> function to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter Interface</a>
 

 

