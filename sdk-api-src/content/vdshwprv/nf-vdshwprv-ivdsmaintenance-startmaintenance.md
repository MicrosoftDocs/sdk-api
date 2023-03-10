---
UID: NF:vdshwprv.IVdsMaintenance.StartMaintenance
title: IVdsMaintenance::StartMaintenance (vdshwprv.h)
description: The IVdsMaintenance::StartMaintenance (vdshwprv.h) method starts a maintenance operation.
helpviewer_keywords: ["IVdsMaintenance interface [VDS]","StartMaintenance method","IVdsMaintenance.StartMaintenance","IVdsMaintenance::StartMaintenance","StartMaintenance","StartMaintenance method [VDS]","StartMaintenance method [VDS]","IVdsMaintenance interface","base.ivdsmaintenance_startmaintenance","vds/IVdsMaintenance::StartMaintenance","vdshwprv/IVdsMaintenance::StartMaintenance"]
old-location: base\ivdsmaintenance_startmaintenance.htm
tech.root: base
ms.assetid: 8d2e1022-ae79-4f71-a488-2c86b43b2a7f
ms.date: 08/08/2022
ms.keywords: IVdsMaintenance interface [VDS],StartMaintenance method, IVdsMaintenance.StartMaintenance, IVdsMaintenance::StartMaintenance, StartMaintenance, StartMaintenance method [VDS], StartMaintenance method [VDS],IVdsMaintenance interface, base.ivdsmaintenance_startmaintenance, vds/IVdsMaintenance::StartMaintenance, vdshwprv/IVdsMaintenance::StartMaintenance
req.header: vdshwprv.h
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
 - IVdsMaintenance::StartMaintenance
 - vdshwprv/IVdsMaintenance::StartMaintenance
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
 - IVdsMaintenance.StartMaintenance
---

# IVdsMaintenance::StartMaintenance


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Starts a maintenance operation.

## -parameters

### -param operation [in]

A maintenance operation enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_maintenance_operation">VDS_MAINTENANCE_OPERATION</a>.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
This return value signals a software or communication problem inside a provider that caches information about the array. Use the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method followed by the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
  
The subsystem object is no longer present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The subsystem is in a failed state, and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress; this operation cannot proceed until the previous operation or operations are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NOT_SUPPORTED</b></dt>
<dt>0x80042400L</dt>
</dl>
</td>
<td width="60%">
This operation or combination of parameters is not supported by this provider. 

</td>
</tr>
</table>

## -remarks

Once an operation begins, it runs until the caller invokes either the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-stopmaintenance">StopMaintenance</a> method or the <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-pulsemaintenance">PulseMaintenance</a> method. When 
        <b>StopMaintenance</b> is called on a running operation, the operation stops immediately. When <b>PulseMaintenance</b> is called on a running operation, the operation pulses the specified number of times and then stops. 


Calling <b>StartMaintenance</b> on a pulsing operation causes the operation to start and run until either <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-stopmaintenance">StopMaintenance</a> is called to stop it or <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-pulsemaintenance">PulseMaintenance</a> is called to set it pulsing it again.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a>



<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsmaintenance">IVdsMaintenance</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-pulsemaintenance">IVdsMaintenance::PulseMaintenance</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsmaintenance-stopmaintenance">IVdsMaintenance::StopMaintenance</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_maintenance_operation">VDS_MAINTENANCE_OPERATION</a>
