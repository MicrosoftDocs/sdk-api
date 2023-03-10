---
UID: NN:iads.IADsFileService
title: IADsFileService (iads.h)
description: The IADsFileService interface is a dual interface that inherits from IADsService.
helpviewer_keywords: ["IADsFileService","IADsFileService interface [ADSI]","IADsFileService interface [ADSI]","described","_ds_iadsfileservice","adsi.iadsfileservice","iads/IADsFileService"]
old-location: adsi\iadsfileservice.htm
tech.root: adsi
ms.assetid: 328eedfe-7fdc-4e90-8bac-ab30944b8fbf
ms.date: 12/05/2018
ms.keywords: IADsFileService, IADsFileService interface [ADSI], IADsFileService interface [ADSI],described, _ds_iadsfileservice, adsi.iadsfileservice, iads/IADsFileService
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
 - IADsFileService
 - iads/IADsFileService
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
 - IADsFileService
---

# IADsFileService interface


## -description

The <b>IADsFileService</b> interface is a dual interface that inherits from  <a href="/windows/desktop/api/iads/nn-iads-iadsservice">IADsService</a>. It is designed for representing file services supported in the directory service. Through this interface you can discover and modify the maximum number of users simultaneously running a file service.
   

To access active sessions or open resources used by the file service, you must go through the  <a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a> interface to retrieve sessions or resources.

To examine the status of the file service or to perform service management operations, you use the  <a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a> interface, which is inherited by <a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.

## -inheritance

The <b>IADsFileService</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>, <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>, and <a href="/windows/desktop/api/iads/nn-iads-iadsservice">IADsService</a>. <b>IADsFileService</b> also has these types of members:

## -remarks

Under the WinNT provider, this interface is implemented on the <b>WinNTService</b> object.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadsfileservice-property-methods">IADsFileService
    Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsservice">IADsService</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsserviceoperations">IADsServiceOperations</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
