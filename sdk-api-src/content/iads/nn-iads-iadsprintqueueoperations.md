---
UID: NN:iads.IADsPrintQueueOperations
title: IADsPrintQueueOperations (iads.h)
description: Used to control a printer from across a network.
helpviewer_keywords: ["IADsPrintQueueOperations","IADsPrintQueueOperations interface [ADSI]","IADsPrintQueueOperations interface [ADSI]","described","_ds_iadsprintqueueoperations","adsi.iadsprintqueueoperations","iads/IADsPrintQueueOperations"]
old-location: adsi\iadsprintqueueoperations.htm
tech.root: adsi
ms.assetid: 97495455-a576-4984-beb8-9282073e88c2
ms.date: 12/05/2018
ms.keywords: IADsPrintQueueOperations, IADsPrintQueueOperations interface [ADSI], IADsPrintQueueOperations interface [ADSI],described, _ds_iadsprintqueueoperations, adsi.iadsprintqueueoperations, iads/IADsPrintQueueOperations
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
 - IADsPrintQueueOperations
 - iads/IADsPrintQueueOperations
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
 - IADsPrintQueueOperations
---

# IADsPrintQueueOperations interface


## -description

The <b>IADsPrintQueueOperations</b> interface is a 
    dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is used to 
    control a printer from across a network.

The <b>IADsPrintQueueOperations</b> interface 
     supports the following operations:
<ul>
<li>Retrieve all print jobs submitted to the print queue.</li>
<li>Suspend the print queue operation.</li>
<li>Resume the print queue operation.</li>
<li>Remove all print jobs from the print queue.</li>
</ul>

## -inheritance

The <b>IADsPrintQueueOperations</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsPrintQueueOperations</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
