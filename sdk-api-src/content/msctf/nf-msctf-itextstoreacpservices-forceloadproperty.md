---
UID: NF:msctf.ITextStoreACPServices.ForceLoadProperty
title: ITextStoreACPServices::ForceLoadProperty
author: windows-sdk-content
description: ITextStoreACPServices::ForceLoadProperty method
old-location: tsf\itextstoreacpservices_forceloadproperty.htm
old-project: TSF
ms.assetid: 6792ccc0-7bbd-479c-9f24-a283ce03c7fe
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ForceLoadProperty, ForceLoadProperty method [Text Services Framework], ForceLoadProperty method [Text Services Framework],ITextStoreACPServices interface, ITextStoreACPServices interface [Text Services Framework],ForceLoadProperty method, ITextStoreACPServices.ForceLoadProperty, ITextStoreACPServices::ForceLoadProperty, _tsf_itextstoreacpservices_forceloadproperty_ref, msctf/ITextStoreACPServices::ForceLoadProperty, tsf.itextstoreacpservices_forceloadproperty
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
 - ITextStoreACPServices.ForceLoadProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITextStoreACPServices::ForceLoadProperty


## -description




## -parameters




### -param pProp [in]

Pointer to an <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> object that specifies the property to load.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

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



When calling this method, the application must be able to grant a synchronous read-only lock.




## -see-also




<a href="https://msdn.microsoft.com/8c84429c-3f99-4ab1-b994-e4e93cd9c86d">ITextStoreACPServices</a>



<a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize
      </a>



<a href="https://msdn.microsoft.com/7d7af737-6241-43a9-946e-6a03a423b20f">
        ITfPersistentPropertyLoaderACP
      </a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">
        ITfProperty
      </a>
 

 

