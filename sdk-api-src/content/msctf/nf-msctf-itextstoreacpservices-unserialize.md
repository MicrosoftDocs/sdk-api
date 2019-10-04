---
UID: NF:msctf.ITextStoreACPServices.Unserialize
title: ITextStoreACPServices::Unserialize (msctf.h)
author: windows-sdk-content
description: ITextStoreACPServices::Unserialize method
old-location: tsf\itextstoreacpservices_unserialize.htm
tech.root: TSF
ms.assetid: 4eb2f2b9-51fb-4970-a195-c05e1d19ff99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreACPServices interface [Text Services Framework],Unserialize method, ITextStoreACPServices.Unserialize, ITextStoreACPServices::Unserialize, Unserialize, Unserialize method [Text Services Framework], Unserialize method [Text Services Framework],ITextStoreACPServices interface, _tsf_itextstoreacpservices_unserialize_ref, msctf/ITextStoreACPServices::Unserialize, tsf.itextstoreacpservices_unserialize
ms.topic: method
f1_keywords: 
 - "msctf/ITextStoreACPServices.Unserialize"
dev_langs:
 - c++
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
 - ITextStoreACPServices.Unserialize
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACPServices::Unserialize


## -description




## -parameters




### -param pProp [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty</a> object that receives the property data.


### -param pHdr [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that contains the header data for the property.


### -param pStream [in]

Pointer to an <b>IStream</b> object that contains the property data. This parameter can be <b>NULL</b> if <i>pLoader</i> is not <b>NULL</b>. This parameter is ignored if <i>pLoader</i> is not <b>NULL</b>.


### -param pLoader [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp">ITfPersistentPropertyLoaderACP</a> object that the TSF manager will use to obtain the property data. This parameter can be <b>NULL</b> if <i>pStream</i> is not <b>NULL</b>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itextstoreacpservices">ITextStoreACPServices</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize">ITextStoreACPServices::Serialize
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfpersistentpropertyloaderacp">ITfPersistentPropertyLoaderACP
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfproperty">ITfProperty
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_persistent_property_header_acp">TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>
 

 

