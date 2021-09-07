---
UID: NN:iads.IADsExtension
title: IADsExtension (iads.h)
description: The IADsExtension interface forms the basis of the ADSI application extension model.
helpviewer_keywords: ["IADsExtension","IADsExtension interface [ADSI]","IADsExtension interface [ADSI]","described","_ds_iadsextension","adsi.iadsextension","iads/IADsExtension"]
old-location: adsi\iadsextension.htm
tech.root: adsi
ms.assetid: 05681526-2232-4341-859d-6773f7a58431
ms.date: 12/05/2018
ms.keywords: IADsExtension, IADsExtension interface [ADSI], IADsExtension interface [ADSI],described, _ds_iadsextension, adsi.iadsextension, iads/IADsExtension
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsExtension
 - iads/IADsExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsExtension
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
     <i>dwCode</i> in the <a href="/windows/desktop/api/iads/nf-iads-iadsextension-operate">Operate</a> 
     method. In this case, an extension client must call the 
     <b>Operate</b> method. The other two methods, namely, 
     <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privateinvoke">PrivateInvoke</a> and 
     <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privategetidsofnames">PrivateGetIDsOfNames</a>, usually 
     return <b>E_NOTIMPL</b> in the <b>HRESULT</b> value.</li>
<li>The extension component supports any dual or dispatch interface. In this case, an extension client must  
     call the <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privategetidsofnames">PrivateGetIDsOfNames</a> or 
     <a href="/windows/desktop/api/iads/nf-iads-iadsextension-privateinvoke">PrivateInvoke</a> methods. 
     <a href="/windows/desktop/api/iads/nf-iads-iadsextension-operate">Operate</a> usually ignores the data and returns 
     <b>E_NOTIMPL</b> in the <b>HRESULT</b> value.</li>
</ul>

## -inheritance

The <b>IADsExtension</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IADsExtension</b> also has these types of members:

