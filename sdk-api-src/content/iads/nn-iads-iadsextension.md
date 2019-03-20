---
UID: NN:iads.IADsExtension
title: IADsExtension (iads.h)
author: windows-sdk-content
description: The IADsExtension interface forms the basis of the ADSI application extension model.
old-location: adsi\iadsextension.htm
tech.root: adsi
ms.assetid: 05681526-2232-4341-859d-6773f7a58431
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsExtension, IADsExtension interface [ADSI], IADsExtension interface [ADSI],described, _ds_iadsextension, adsi.iadsextension, iads/IADsExtension
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsExtension interface


## -description


The <b>IADsExtension</b> interface forms the basis of the ADSI 
    application extension model. It enables an independent software vendor (ISV) to add application-specific 
    behaviors, such as methods or functions, into an existing ADSI object. Multiple vendors can independently extend 
    the features of the same object to perform similar, but unrelated operations.

The extension model is based on the aggregation model in COM. An aggregator, or outer object, can add to its 
    base of methods, those of an aggregate object, or inner object. An ADSI extension object, which implements the 
    <b>IADsExtension</b> interface, is an aggregate object, whereas an 
    ADSI provider is an aggregator.
<div class="alert"><b>Note</b>  When implementing an extension module, release an interface when finished with it. Otherwise, the aggregator 
    cannot release the interface even when no longer required.</div><div> </div>The <b>IADsExtension</b> interface can be used as follows:
<ul>
<li>The extension component requires an initialization notification as defined by 
     <i>dwCode</i> in the <a href="https://msdn.microsoft.com/c3cab311-6717-4d95-ad46-9da6047f84b8">Operate</a> 
     method. In this case, an extension client must call the 
     <b>Operate</b> method. The other two methods, namely, 
     <a href="https://msdn.microsoft.com/5af74a05-df64-4679-890b-a5a031633fd8">PrivateInvoke</a> and 
     <a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">PrivateGetIDsOfNames</a>, usually 
     return <b>E_NOTIMPL</b> in the <b>HRESULT</b> value.</li>
<li>The extension component supports any dual or dispatch interface. In this case, an extension client must  
     call the <a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">PrivateGetIDsOfNames</a> or 
     <a href="https://msdn.microsoft.com/5af74a05-df64-4679-890b-a5a031633fd8">PrivateInvoke</a> methods. 
     <a href="https://msdn.microsoft.com/c3cab311-6717-4d95-ad46-9da6047f84b8">Operate</a> usually ignores the data and returns 
     <b>E_NOTIMPL</b> in the <b>HRESULT</b> value.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsExtension</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IADsExtension</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsExtension</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3cab311-6717-4d95-ad46-9da6047f84b8">Operate</a>
</td>
<td align="left" width="63%">
Performs the specified extended operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/533faef7-d504-443c-83e7-7eaf461ce550">PrivateGetIDsOfNames</a>
</td>
<td align="left" width="63%">
Maps the name(s) to a DISPID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5af74a05-df64-4679-890b-a5a031633fd8">PrivateInvoke</a>
</td>
<td align="left" width="63%">
Invokes methods of the extended object.

</td>
</tr>
</table> 

