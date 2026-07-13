---
UID: NF:vds.IVdsVolumeMF3.OfflineVolume
title: IVdsVolumeMF3::OfflineVolume (vds.h)
description: Takes the volume offline by using the IOCTL_VOLUME_OFFLINE control code.
helpviewer_keywords: ["IVdsVolumeMF3 interface","OfflineVolume method","IVdsVolumeMF3.OfflineVolume","IVdsVolumeMF3::OfflineVolume","OfflineVolume","OfflineVolume method","OfflineVolume method","IVdsVolumeMF3 interface","base.ivdsvolumemf3_offlinevolume","vds/IVdsVolumeMF3::OfflineVolume"]
old-location: base\ivdsvolumemf3_offlinevolume.htm
tech.root: base
ms.assetid: d7f699c6-6f1c-445d-80b4-3576102d5b5f
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF3 interface,OfflineVolume method, IVdsVolumeMF3.OfflineVolume, IVdsVolumeMF3::OfflineVolume, OfflineVolume, OfflineVolume method, OfflineVolume method,IVdsVolumeMF3 interface, base.ivdsvolumemf3_offlinevolume, vds/IVdsVolumeMF3::OfflineVolume
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsVolumeMF3::OfflineVolume
 - vds/IVdsVolumeMF3::OfflineVolume
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
 - IVdsVolumeMF3.OfflineVolume
---

# IVdsVolumeMF3::OfflineVolume


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Takes the volume offline by using the <a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_volume_offline">IOCTL_VOLUME_OFFLINE</a> control code.



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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>

## -remarks

If the volume is already offline, the <b>OfflineVolume</b> method returns S_OK.

When a volume is offline, all read, write, and IOCTL requests fail with 
    <b>ERROR_NOT_READY</b>. You cannot take the system or boot volume offline.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online 
    is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the 
    dismounted volume from being mounted again. To dismount a volume, use the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-dismount">IVdsVolumeMF::Dismount</a> method.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf3">IVdsVolumeMF3</a>
