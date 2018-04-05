---
UID: NF:msctf.ITextStoreACPServices.Unserialize
title: ITextStoreACPServices::Unserialize method
author: windows-driver-content
description: ITextStoreACPServices::Unserialize method
old-location: tsf\itextstoreacpservices_unserialize.htm
old-project: TSF
ms.assetid: 4eb2f2b9-51fb-4970-a195-c05e1d19ff99
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITextStoreACPServices, ITextStoreACPServices interface [Text Services Framework], Unserialize method, ITextStoreACPServices::Unserialize, Unserialize method [Text Services Framework], Unserialize method [Text Services Framework], ITextStoreACPServices interface, Unserialize,ITextStoreACPServices.Unserialize, _tsf_itextstoreacpservices_unserialize_ref, msctf/ITextStoreACPServices::Unserialize, tsf.itextstoreacpservices_unserialize
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
-	ITextStoreACPServices.Unserialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITextStoreACPServices::Unserialize method


## -description




## -parameters




### -param pProp [in]

Pointer to an <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> object that receives the property data.


### -param pHdr [in]

Pointer to a <a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that contains the header data for the property.


### -param pStream [in]

Pointer to an <b>IStream</b> object that contains the property data. This parameter can be <b>NULL</b> if <i>pLoader</i> is not <b>NULL</b>. This parameter is ignored if <i>pLoader</i> is not <b>NULL</b>.


### -param pLoader [in]

Pointer to an <a href="https://msdn.microsoft.com/7d7af737-6241-43a9-946e-6a03a423b20f">ITfPersistentPropertyLoaderACP</a> object that the TSF manager will use to obtain the property data. This parameter can be <b>NULL</b> if <i>pStream</i> is not <b>NULL</b>.


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
<dt><b>TF_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The property data will be obtained asynchronously.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_SYNCHRONOUS</b></dt>
</dl>
</td>
<td width="60%">
A synchronous read-only lock cannot be obtained.

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



If <i>pStream</i> is specified rather than <i>pLoader</i>, the property data will be read from <i>pStream</i> during the call to <b>Unserialize</b> . If <i>pLoader</i> is specified rather than <i>pStream</i>, the property data will be read from <i>pLoader</i> asynchronously. Using <i>pStream</i> can cause long delays if the property data is large.

While calling this method, the application must be able to grant a synchronous read-only lock.




## -see-also




<a href="https://msdn.microsoft.com/8c84429c-3f99-4ab1-b994-e4e93cd9c86d">ITextStoreACPServices</a>



<a href="https://msdn.microsoft.com/14be52d1-4f8c-4deb-aa92-470c3608c841">
        ITextStoreACPServices::Serialize
      </a>



<a href="https://msdn.microsoft.com/7d7af737-6241-43a9-946e-6a03a423b20f">
        ITfPersistentPropertyLoaderACP
      </a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty
      </a>



<a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">
        TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>
 

 

