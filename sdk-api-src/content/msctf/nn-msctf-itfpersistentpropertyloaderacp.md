---
UID: NN:msctf.ITfPersistentPropertyLoaderACP
title: ITfPersistentPropertyLoaderACP (msctf.h)
author: windows-sdk-content
description: The ITfPersistentPropertyLoaderACP interface is implemented by an application and used by the TSF manager to load properties asynchronously.
old-location: tsf\itfpersistentpropertyloaderacp.htm
tech.root: TSF
ms.assetid: 7d7af737-6241-43a9-946e-6a03a423b20f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfPersistentPropertyLoaderACP, ITfPersistentPropertyLoaderACP interface [Text Services Framework], ITfPersistentPropertyLoaderACP interface [Text Services Framework],described, _tsf_itfpersistentpropertyloaderacp_ref, msctf/ITfPersistentPropertyLoaderACP, tsf.itfpersistentpropertyloaderacp
ms.topic: interface
f1_keywords: 
 - "msctf/ITfPersistentPropertyLoaderACP"
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
 - ITfPersistentPropertyLoaderACP
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfPersistentPropertyLoaderACP interface


## -description


The <b>ITfPersistentPropertyLoaderACP</b> interface is implemented by an application and used by the TSF manager to load properties asynchronously. An application passes an instance of this interface when calling <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize</a>. When properties are loaded by a call to <b>ITextStoreACPServices::Unserialize</b> , this interface is used to load properties when required rather than all at once.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPersistentPropertyLoaderACP</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfPersistentPropertyLoaderACP</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfpersistentpropertyloaderacp-loadproperty">LoadProperty</a>
</td>
<td align="left" width="63%">
Called to load a property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">ITextStoreACPServices::Unserialize
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

