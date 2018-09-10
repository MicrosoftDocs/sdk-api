---
UID: NF:msctf.ITfContextOwnerServices.Serialize
title: ITfContextOwnerServices::Serialize
author: windows-sdk-content
description: The ITfContextOwnerServices::Serialize method obtains a property from a range of text and writes the property data into a stream object. This enables an application to store property data, for example, when writing the data to a file.
old-location: tsf\itfcontextownerservices_serialize.htm
tech.root: TSF
ms.assetid: e67b6fa7-610d-426f-a290-36c0da4068f4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],Serialize method, ITfContextOwnerServices.Serialize, ITfContextOwnerServices::Serialize, Serialize, Serialize method [Text Services Framework], Serialize method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_serialize_ref, msctf/ITfContextOwnerServices::Serialize, tsf.itfcontextownerservices_serialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerServices.Serialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextOwnerServices::Serialize


## -description


The <b>ITfContextOwnerServices::Serialize</b> method obtains a property from a range of text and writes the property data into a stream object. This enables an application to store property data, for example, when writing the data to a file.


## -parameters




### -param pProp [in]

Pointer to an <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> interface that identifies the property to serialize.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that identifies the range that the property is obtained from.


### -param pHdr [out]

Pointer to a <a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that receives the header data for the property.


### -param pStream [in]

Pointer to an <b>IStream</b> object that the TSF manager will write the property data to.


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
The property cannot be serialized.

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
</table>
 




## -remarks



The property header data placed in <i>pHdr</i> is common to all properties and must be preserved with the data written into <i>pStream</i>. This same data pair must be passed to <a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITfContextOwnerServices::Unserialize</a> to restore the property data.

An application can save all of the properties for the entire document by performing the following steps.

<ul>
<li>Enumerate all properties using <a href="https://msdn.microsoft.com/b57c9fdc-320b-4d97-8af4-c75756326437">ITfContext::EnumProperties</a>.</li>
<li>Within each property, enumerate the ranges using <a href="https://msdn.microsoft.com/201c518b-f06f-4c4f-aa56-f8d21f477814">ITfReadOnlyProperty::EnumRanges</a>.</li>
<li>Pass the current property and range to this method.</li>
<li>Write the data placed in <i>pHdr</i> to the file.</li>
<li>Write the data added to <i>pStream</i> to the file.</li>
</ul>
When calling this method, the application must be able to grant a synchronous read-only lock.




## -see-also




<a href="https://msdn.microsoft.com/fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86">ITfContextOwnerServices</a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>
 

 

