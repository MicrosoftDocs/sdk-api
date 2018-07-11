---
UID: NF:msctf.ITfPersistentPropertyLoaderACP.LoadProperty
title: ITfPersistentPropertyLoaderACP::LoadProperty
author: windows-sdk-content
description: ITfPersistentPropertyLoaderACP::LoadProperty method
old-location: tsf\itfpersistentpropertyloaderacp_loadproperty.htm
old-project: TSF
ms.assetid: 20730a90-e59c-46ae-a0bf-a212b201351c
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfPersistentPropertyLoaderACP interface [Text Services Framework],LoadProperty method, ITfPersistentPropertyLoaderACP.LoadProperty, ITfPersistentPropertyLoaderACP::LoadProperty, LoadProperty, LoadProperty method [Text Services Framework], LoadProperty method [Text Services Framework],ITfPersistentPropertyLoaderACP interface, _tsf_itfpersistentpropertyloaderacp_loadproperty_ref, msctf/ITfPersistentPropertyLoaderACP::LoadProperty, tsf.itfpersistentpropertyloaderacp_loadproperty
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
 - Msctf.dll
api_name:
 - ITfPersistentPropertyLoaderACP.LoadProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfPersistentPropertyLoaderACP::LoadProperty


## -description




## -parameters




### -param pHdr [in]

Pointer to a <a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that identifies the property to load. This structure contains the same data as the structure passed to <a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize</a>.


### -param ppStream [out]

Pointer to an <b>IStream</b> interface pointer that receives the stream object.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



Only property data is written to the stream. The header data is not written to the stream.

Obtain the original position of the stream before writing to the stream. The original position should be restored in the stream before returning from this method.




## -see-also




<a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize
      </a>



<a href="https://msdn.microsoft.com/7d7af737-6241-43a9-946e-6a03a423b20f">ITfPersistentPropertyLoaderACP</a>



<a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">
        TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>
 

 

