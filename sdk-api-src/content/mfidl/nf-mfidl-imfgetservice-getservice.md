---
UID: NF:mfidl.IMFGetService.GetService
title: IMFGetService::GetService (mfidl.h)
description: Retrieves a service interface.
helpviewer_keywords: ["4287dd1f-1718-4231-bc62-b58e0e61d688","GetService","GetService method [Media Foundation]","GetService method [Media Foundation]","IMFGetService interface","IMFGetService interface [Media Foundation]","GetService method","IMFGetService.GetService","IMFGetService::GetService","mf.imfgetservice_getservice","mfidl/IMFGetService::GetService"]
old-location: mf\imfgetservice_getservice.htm
tech.root: mf
ms.assetid: 4287dd1f-1718-4231-bc62-b58e0e61d688
ms.date: 12/05/2018
ms.keywords: 4287dd1f-1718-4231-bc62-b58e0e61d688, GetService, GetService method [Media Foundation], GetService method [Media Foundation],IMFGetService interface, IMFGetService interface [Media Foundation],GetService method, IMFGetService.GetService, IMFGetService::GetService, mf.imfgetservice_getservice, mfidl/IMFGetService::GetService
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFGetService::GetService
 - mfidl/IMFGetService::GetService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFGetService.GetService
---

# IMFGetService::GetService


## -description

Retrieves a service interface.

## -parameters

### -param guidService [in]

The service identifier (SID) of the service. For a list of service identifiers, see <a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>.

### -param riid [in]

The interface identifier (IID) of the interface being requested.

### -param ppvObject [out]

Receives the interface pointer. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the service.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice">IMFGetService</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfgetservice">MFGetService</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>