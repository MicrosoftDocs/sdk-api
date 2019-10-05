---
UID: NN:msctf.ITextStoreACPServices
title: ITextStoreACPServices (msctf.h)
author: windows-sdk-content
description: The ITextStoreACPServices interface is implemented by the TSF manager to provide various services to an ACP-based application.
old-location: tsf\itextstoreacpservices.htm
tech.root: TSF
ms.assetid: 8c84429c-3f99-4ab1-b994-e4e93cd9c86d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreACPServices, ITextStoreACPServices interface [Text Services Framework], ITextStoreACPServices interface [Text Services Framework],described, _tsf_itextstoreacpservices_ref, msctf/ITextStoreACPServices, tsf.itextstoreacpservices
ms.topic: interface
f1_keywords: 
 - "msctf/ITextStoreACPServices"
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
 - ITextStoreACPServices
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACPServices interface


## -description


The <b>ITextStoreACPServices</b> interface is implemented by the TSF manager to provide various services to an ACP-based application. To obtain an instance of this interface, an application calls <b>QueryInterface</b> on the <i>punk</i> parameter passed to <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink</a> with IID_ITextStoreACPServices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACPServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStoreACPServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreACPServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-createrange">CreateRange</a>
</td>
<td align="left" width="63%">
Creates a range object from two ACP values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-forceloadproperty">ForceLoadProperty</a>
</td>
<td align="left" width="63%">
Forces all values of an asynchronously loaded property to be loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Obtains a property from a range of text and writes the property data into a stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itextstoreacpservices-unserialize">Unserialize</a>
</td>
<td align="left" width="63%">
Takes previously serialized property data and applies it to a property object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-advisesink">ITextStoreACP::AdviseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

