---
UID: NN:msctf.ITfPersistentPropertyLoaderACP
title: ITfPersistentPropertyLoaderACP
author: windows-sdk-content
description: The ITfPersistentPropertyLoaderACP interface is implemented by an application and used by the TSF manager to load properties asynchronously.
old-location: tsf\itfpersistentpropertyloaderacp.htm
old-project: TSF
ms.assetid: 7d7af737-6241-43a9-946e-6a03a423b20f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfPersistentPropertyLoaderACP, ITfPersistentPropertyLoaderACP interface [Text Services Framework], ITfPersistentPropertyLoaderACP interface [Text Services Framework],described, _tsf_itfpersistentpropertyloaderacp_ref, msctf/ITfPersistentPropertyLoaderACP, tsf.itfpersistentpropertyloaderacp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITfPersistentPropertyLoaderACP
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfPersistentPropertyLoaderACP interface


## -description


The <b>ITfPersistentPropertyLoaderACP</b> interface is implemented by an application and used by the TSF manager to load properties asynchronously. An application passes an instance of this interface when calling <a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize</a>. When properties are loaded by a call to <b>ITextStoreACPServices::Unserialize</b> , this interface is used to load properties when required rather than all at once.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPersistentPropertyLoaderACP</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfPersistentPropertyLoaderACP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfPersistentPropertyLoaderACP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20730a90-e59c-46ae-a0bf-a212b201351c">LoadProperty</a>
</td>
<td align="left" width="63%">
Called to load a property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

