---
UID: NF:vds.IVdsHbaPort.SetAllPathStatuses
title: IVdsHbaPort::SetAllPathStatuses (vds.h)
description: Sets the statuses of all paths originating from the HBA port to a specified status.
helpviewer_keywords: ["IVdsHbaPort interface [VDS]","SetAllPathStatuses method","IVdsHbaPort.SetAllPathStatuses","IVdsHbaPort::SetAllPathStatuses","SetAllPathStatuses","SetAllPathStatuses method [VDS]","SetAllPathStatuses method [VDS]","IVdsHbaPort interface","base.ivdshbaport_setallpathstatuses","vds/IVdsHbaPort::SetAllPathStatuses"]
old-location: base\ivdshbaport_setallpathstatuses.htm
tech.root: base
ms.assetid: 0df5b5f7-1fdc-41f1-96e4-2abe96c59228
ms.date: 12/05/2018
ms.keywords: IVdsHbaPort interface [VDS],SetAllPathStatuses method, IVdsHbaPort.SetAllPathStatuses, IVdsHbaPort::SetAllPathStatuses, SetAllPathStatuses, SetAllPathStatuses method [VDS], SetAllPathStatuses method [VDS],IVdsHbaPort interface, base.ivdshbaport_setallpathstatuses, vds/IVdsHbaPort::SetAllPathStatuses
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsHbaPort::SetAllPathStatuses
 - vds/IVdsHbaPort::SetAllPathStatuses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
api_name:
 - IVdsHbaPort.SetAllPathStatuses
---

# IVdsHbaPort::SetAllPathStatuses


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Sets the statuses of all paths originating from the HBA port to a specified status.

## -parameters

### -param status

The status to be assigned to the paths.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The statuses were successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_STATUSES_INCOMPLETELY_SET</b></dt>
<dt>0x00042702L</dt>
</dl>
</td>
<td width="60%">
At least one path's status was not set successfully due to a nonfatal error (for example, the status 
        conflicts with the current load balance policy).

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdshbaport">IVdsHbaPort</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_path_status">VDS_PATH_STATUS</a>