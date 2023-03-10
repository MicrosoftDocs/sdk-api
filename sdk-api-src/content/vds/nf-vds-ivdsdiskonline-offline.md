---
UID: NF:vds.IVdsDiskOnline.Offline
title: IVdsDiskOnline::Offline (vds.h)
description: Takes the disk offline.Windows Vista:  This method is not supported until Windows Vista with Service Pack 1 (SP1). Use IVdsDisk2::SetSANMode instead.
helpviewer_keywords: ["IVdsDiskOnline interface","Offline method","IVdsDiskOnline.Offline","IVdsDiskOnline::Offline","Offline","Offline method","Offline method","IVdsDiskOnline interface","base.ivdsdiskonline_offline","vds/IVdsDiskOnline::Offline"]
old-location: base\ivdsdiskonline_offline.htm
tech.root: base
ms.assetid: 3f27dd46-2fa1-4522-9d35-db78255c6d11
ms.date: 12/05/2018
ms.keywords: IVdsDiskOnline interface,Offline method, IVdsDiskOnline.Offline, IVdsDiskOnline::Offline, Offline, Offline method, Offline method,IVdsDiskOnline interface, base.ivdsdiskonline_offline, vds/IVdsDiskOnline::Offline
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsDiskOnline::Offline
 - vds/IVdsDiskOnline::Offline
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
 - IVdsDiskOnline.Offline
---

# IVdsDiskOnline::Offline


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Takes the disk offline.<b>Windows Vista:  </b>This method is not supported until Windows Vista with Service Pack 1 (SP1). Use <a href="/windows/desktop/api/vds/nf-vds-ivdsdisk2-setsanmode">IVdsDisk2::SetSANMode</a> instead.



## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FAILED_TO_OFFLINE_DISK</b></dt>
</dl>
</td>
<td width="60%">
The offline operation failed.

</td>
</tr>
</table>

## -remarks

If a dynamic disk is read/write and online, it can be made read-only and taken offline as follows:

<ol>
<li>For each volume on the disk, call the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-dismount">IVdsVolumeMF::Dismount</a> method, setting the <i>bForce</i> and <i>bPermanent</i> parameters to <b>TRUE</b>.</li>
<li>Call the <b>Offline</b> method.</li>
<li>Set the read-only bit. (This is the <b>VDS_DF_READ_ONLY</b> flag in the <a href="/windows/desktop/api/vds/ns-vds-vds_disk_prop">VDS_DISK_PROP</a> structure.)</li>
</ol>
If a basic disk is read/write and online, it can be made read-only and taken offline the same way, but the order of the steps does not matter.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsdiskonline">IVdsDiskOnline</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsdiskonline-online">IVdsDiskOnline::Online</a>
