---
UID: NF:vds.IVdsService.Reboot
title: IVdsService::Reboot (vds.h)
description: Restarts the computer hosting the provider.
helpviewer_keywords: ["IVdsService interface [VDS]","Reboot method","IVdsService.Reboot","IVdsService::Reboot","Reboot","Reboot method [VDS]","Reboot method [VDS]","IVdsService interface","base.ivdsservice_reboot","vds/IVdsService::Reboot"]
old-location: base\ivdsservice_reboot.htm
tech.root: base
ms.assetid: c22be0a5-d7ed-4f76-961d-2455ca99f220
ms.date: 12/05/2018
ms.keywords: IVdsService interface [VDS],Reboot method, IVdsService.Reboot, IVdsService::Reboot, Reboot, Reboot method [VDS], Reboot method [VDS],IVdsService interface, base.ivdsservice_reboot, vds/IVdsService::Reboot
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
 - IVdsService::Reboot
 - vds/IVdsService::Reboot
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
 - IVdsService.Reboot
---

# IVdsService::Reboot


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Restarts the computer hosting the provider.



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
The method completed successfully.

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
VDS failed to initialize. If an application calls this method before the service finishes initializing, the method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>

## -remarks

This method displays the following message to the user:

"Virtual Disk Service: Operation requires that the computer be restarted."

VDS prompts the user to save their current work and exit before the system shuts down. <b>Reboot</b> does not force an application in operation to close.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>
