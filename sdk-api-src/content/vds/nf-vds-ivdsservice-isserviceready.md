---
UID: NF:vds.IVdsService.IsServiceReady
title: IVdsService::IsServiceReady (vds.h)
description: Returns the initialization status of VDS.
helpviewer_keywords: ["IVdsService interface [VDS]","IsServiceReady method","IVdsService.IsServiceReady","IVdsService::IsServiceReady","IsServiceReady","IsServiceReady method [VDS]","IsServiceReady method [VDS]","IVdsService interface","base.ivdsservice_isserviceready","vds/IVdsService::IsServiceReady"]
old-location: base\ivdsservice_isserviceready.htm
tech.root: base
ms.assetid: 79ef68db-6bc6-40b3-a133-86f00eb70ee3
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],IsServiceReady method, IVdsService.IsServiceReady, IVdsService::IsServiceReady, IsServiceReady, IsServiceReady method [VDS], IsServiceReady method [VDS],IVdsService interface, base.ivdsservice_isserviceready, vds/IVdsService::IsServiceReady
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
 - IVdsService::IsServiceReady
 - vds/IVdsService::IsServiceReady
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
 - IVdsService.IsServiceReady
---

# IVdsService::IsServiceReady


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the initialization status of VDS.



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
The initialization completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
VDS has not finished the initialization and the service is not ready.

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
The initialization failed.

</td>
</tr>
</table>

## -remarks

Callers must wait for the initialization process to complete before invoking other VDS methods.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-waitforserviceready">IVdsService::WaitForServiceReady</a>
