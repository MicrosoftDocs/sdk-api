---
UID: NF:vds.IVdsVolumeOnline.Online
title: IVdsVolumeOnline::Online (vds.h)
description: Returns a volume to the healthy state, if possible. This method is supported only for dynamic disks.
helpviewer_keywords: ["IVdsVolumeOnline interface","Online method","IVdsVolumeOnline.Online","IVdsVolumeOnline::Online","Online","Online method","Online method","IVdsVolumeOnline interface","base.ivdsvolumeonline_online","vds/IVdsVolumeOnline::Online"]
old-location: base\ivdsvolumeonline_online.htm
tech.root: base
ms.assetid: 8a207e61-5a13-41ad-bad9-11ddf2844a9b
ms.date: 12/05/2018
ms.keywords: IVdsVolumeOnline interface,Online method, IVdsVolumeOnline.Online, IVdsVolumeOnline::Online, Online, Online method, Online method,IVdsVolumeOnline interface, base.ivdsvolumeonline_online, vds/IVdsVolumeOnline::Online
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IVdsVolumeOnline::Online
 - vds/IVdsVolumeOnline::Online
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
 - IVdsVolumeOnline.Online
---

# IVdsVolumeOnline::Online


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a volume to the healthy state, if possible. This method is supported only for dynamic disks.



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
<dt><b>VDS_S_NO_NOTIFICATION</b></dt>
<dt>0x00042517L</dt>
</dl>
</td>
<td width="60%">
No volume arrival notification was received. You may need to call <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-refresh">IVdsService::Refresh</a>.

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
This method is not supported for basic disks.

</td>
</tr>
</table>

## -remarks

Despite its name, this method does not bring a volume online. It attempts to return a volume on a dynamic disk to a healthy state. 

This method checks whether the volume has a missing disk, plex, or RAID-5 column and attempts to make any needed repairs. 

To bring the volume online, call <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-mount">IVdsVolumeMF::Mount</a>.

To take the volume offline, call <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-dismount">IVdsVolumeMF::Dismount</a> with the <i>bPermanent</i> parameter set to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumeonline">IVdsVolumeOnline</a>
