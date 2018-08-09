---
UID: NF:vds.IVdsService.CleanupObsoleteMountPoints
title: IVdsService::CleanupObsoleteMountPoints
author: windows-sdk-content
description: Removes user-mode paths and mounted folders for volumes that no longer exist.
old-location: base\ivdsservice_cleanupobsoletemountpoints.htm
old-project: vds
ms.assetid: 93ed7789-be60-422c-be4f-e70e16d26fce
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CleanupObsoleteMountPoints, CleanupObsoleteMountPoints method [VDS], CleanupObsoleteMountPoints method [VDS],IVdsService interface, IVdsService interface [VDS],CleanupObsoleteMountPoints method, IVdsService.CleanupObsoleteMountPoints, IVdsService::CleanupObsoleteMountPoints, base.ivdsservice_cleanupobsoletemountpoints, vds/IVdsService::CleanupObsoleteMountPoints
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VDS_VOLUME_TYPE
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
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsService::CleanupObsoleteMountPoints


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Removes user-mode paths and mounted folders for volumes that no longer exist.


## -parameters






## -returns



This method can return standard <b>HRESULT</b> values, such as 
      <b>E_INVALIDARG</b> or <b>E_OUTOFMEMORY</b>, and 
      <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. 
      It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a> 
      using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can 
      originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> 
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
    <i>x</i>:\<i>MountVolume1</i> on <i>Disk2</i>, the 
    \<i>MountVolume1</i> folder on <i>Disk2</i> is also deleted.




## -see-also




<a href="https://msdn.microsoft.com/6b081cc8-fe06-427f-b06d-831a1f1fef52">IVdsService</a>
 

 

