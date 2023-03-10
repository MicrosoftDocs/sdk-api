---
UID: NN:iads.IADsServiceOperations
title: IADsServiceOperations (iads.h)
description: The IADsServiceOperations interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsServiceOperations","IADsServiceOperations interface [ADSI]","IADsServiceOperations interface [ADSI]","described","_ds_iadsserviceoperations","adsi.iadsserviceoperations","iads/IADsServiceOperations"]
old-location: adsi\iadsserviceoperations.htm
tech.root: adsi
ms.assetid: f2459ca2-8a14-4343-bec6-ef3775dbf415
ms.date: 12/05/2018
ms.keywords: IADsServiceOperations, IADsServiceOperations interface [ADSI], IADsServiceOperations interface [ADSI],described, _ds_iadsserviceoperations, adsi.iadsserviceoperations, iads/IADsServiceOperations
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
 - IADsServiceOperations
 - iads/IADsServiceOperations
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
 - IADsServiceOperations
---

# IADsServiceOperations interface


## -description

The <b>IADsServiceOperations</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to manage system services installed on a computer. You can use this interface to start, pause, and stop a system service, change the password, and examine the status of a given service across a network.
   

Of the system services and their operations, file service and file service operations are a special case. They are represented and managed by  <a href="/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a> and  <a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.

## -inheritance

The <b>IADsServiceOperations</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsServiceOperations</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsfileservice">IADsFileService</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
