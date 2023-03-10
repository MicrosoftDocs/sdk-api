---
UID: NF:vds.IVdsService.WaitForServiceReady
title: IVdsService::WaitForServiceReady (vds.h)
description: Waits for VDS initialization to complete and returns the status of the VDS initialization.
helpviewer_keywords: ["IVdsService interface [VDS]","WaitForServiceReady method","IVdsService.WaitForServiceReady","IVdsService::WaitForServiceReady","WaitForServiceReady","WaitForServiceReady method [VDS]","WaitForServiceReady method [VDS]","IVdsService interface","base.ivdsservice_waitforserviceready","vds/IVdsService::WaitForServiceReady"]
old-location: base\ivdsservice_waitforserviceready.htm
tech.root: base
ms.assetid: 85075abe-7fac-40aa-a93e-19d89c0fd760
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],WaitForServiceReady method, IVdsService.WaitForServiceReady, IVdsService::WaitForServiceReady, WaitForServiceReady, WaitForServiceReady method [VDS], WaitForServiceReady method [VDS],IVdsService interface, base.ivdsservice_waitforserviceready, vds/IVdsService::WaitForServiceReady
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsService::WaitForServiceReady
 - vds/IVdsService::WaitForServiceReady
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsService.WaitForServiceReady
---

# IVdsService::WaitForServiceReady


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Waits for VDS initialization to complete and returns the status of the VDS initialization.



## -returns

This method can return standard HRESULT values, such as E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
VDS initialized successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
VDS failed to initialize.

</td>
</tr>
</table>

## -remarks

VDS must initialize successfully before an application can call the methods exposed by VDS objects.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>
