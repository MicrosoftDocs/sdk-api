---
UID: NN:iads.IADsPrintJobOperations
title: IADsPrintJobOperations (iads.h)
description: The IADsPrintJobOperations interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsPrintJobOperations","IADsPrintJobOperations interface [ADSI]","IADsPrintJobOperations interface [ADSI]","described","_ds_iadsprintjoboperations","adsi.iadsprintjoboperations","iads/IADsPrintJobOperations"]
old-location: adsi\iadsprintjoboperations.htm
tech.root: adsi
ms.assetid: 259f6c3d-73ec-4110-801a-c83ffca0f830
ms.date: 12/05/2018
ms.keywords: IADsPrintJobOperations, IADsPrintJobOperations interface [ADSI], IADsPrintJobOperations interface [ADSI],described, _ds_iadsprintjoboperations, adsi.iadsprintjoboperations, iads/IADsPrintJobOperations
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
 - IADsPrintJobOperations
 - iads/IADsPrintJobOperations
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
 - IADsPrintJobOperations
---

# IADsPrintJobOperations interface


## -description

The <b>IADsPrintJobOperations</b> interface is a dual 
    interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is used to control a print job 
    across a network. A print job object that implements the 
    <a href="/windows/desktop/api/iads/nn-iads-iadsprintjob">IADsPrintJob</a> interface will also support the following 
    features for this interface:
<ul>
<li>To examine the operational status and other information.</li>
<li>To interrupt a running print job.</li>
<li>To resume a paused print job.</li>
</ul>

## -inheritance

The <b>IADsPrintJobOperations</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsPrintJobOperations</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsprintjob">IADsPrintJob</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
