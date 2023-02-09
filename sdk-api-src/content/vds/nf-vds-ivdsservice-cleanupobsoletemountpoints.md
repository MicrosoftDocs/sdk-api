---
UID: NF:vds.IVdsService.CleanupObsoleteMountPoints
title: IVdsService::CleanupObsoleteMountPoints (vds.h)
description: Removes user-mode paths and mounted folders for volumes that no longer exist.
helpviewer_keywords: ["CleanupObsoleteMountPoints","CleanupObsoleteMountPoints method [VDS]","CleanupObsoleteMountPoints method [VDS]","IVdsService interface","IVdsService interface [VDS]","CleanupObsoleteMountPoints method","IVdsService.CleanupObsoleteMountPoints","IVdsService::CleanupObsoleteMountPoints","base.ivdsservice_cleanupobsoletemountpoints","vds/IVdsService::CleanupObsoleteMountPoints"]
old-location: base\ivdsservice_cleanupobsoletemountpoints.htm
tech.root: base
ms.assetid: 93ed7789-be60-422c-be4f-e70e16d26fce
ms.date: 12/05/2018
ms.keywords: CleanupObsoleteMountPoints, CleanupObsoleteMountPoints method [VDS], CleanupObsoleteMountPoints method [VDS],IVdsService interface, IVdsService interface [VDS],CleanupObsoleteMountPoints method, IVdsService.CleanupObsoleteMountPoints, IVdsService::CleanupObsoleteMountPoints, base.ivdsservice_cleanupobsoletemountpoints, vds/IVdsService::CleanupObsoleteMountPoints
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
 - IVdsService::CleanupObsoleteMountPoints
 - vds/IVdsService::CleanupObsoleteMountPoints
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
 - IVdsService.CleanupObsoleteMountPoints
---

# IVdsService::CleanupObsoleteMountPoints


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Removes user-mode paths and mounted folders for volumes that no longer exist.



## -returns

This method can return standard <b>HRESULT</b> values, such as 
      <b>E_INVALIDARG</b> or <b>E_OUTOFMEMORY</b>, and 
      <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. 
      It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a> 
      using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can 
      originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> 
      that is being used. Possible return values include the following.

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
Outdated user-mode paths and mounted folders were removed successfully.

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
VDS failed to initialize. If an application calls this method before the service finishes initializing, 
        the method is blocked until the initialization completes. If the initialization fails, this error is 
        returned.

</td>
</tr>
</table>

## -remarks

By default, the registry retains the drive-letter mapping information for uninstalled volumes. If the disk 
    that contains the volume is removed from the computer, the registry entry is retained, so that if the disk and 
    volume return to the same computer, the volume receives the same drive letter. If the disk is moved to a new 
    computer, the registry entries do not move with it, so the volume might receive a different drive letter and 
    volume GUID.

The 
    <b>CleanupObsoleteMountPoints</b> 
    method removes these registry entries. There are three types of registry entries that are removed:

<ul>
<li>If the volume does not have a drive letter or a volume GUID, it has a "no drive letter" 
      registry entry, which is removed by this method.</li>
<li>Otherwise, the volume has registry entries for a volume GUID and possibly a drive letter. Both are removed 
      by this method.</li>
</ul>
In addition, if the volume contains any mounted folders, 
    <b>CleanupObsoleteMountPoints</b> 
    removes them. For example, if <i>Volume1</i> on <i>Disk1</i> is being 
    removed and <i>Volume1</i> is mounted as 
    <i>x</i>:&#92;<i>MountVolume1</i> on <i>Disk2</i>, the 
    &#92;<i>MountVolume1</i> folder on <i>Disk2</i> is also deleted.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>
