---
UID: NF:vds.IVdsOpenVDisk.Compact
title: IVdsOpenVDisk::Compact
author: windows-sdk-content
description: Compacts the virtual disk to reduce the physical size of the backing file.
old-location: base\ivdsopenvdisk_compact.htm
tech.root: VDS
ms.assetid: 011adaae-3a17-4643-ae8d-400753019c83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Compact, Compact method, Compact method,IVdsOpenVDisk interface, IVdsOpenVDisk interface,Compact method, IVdsOpenVDisk.Compact, IVdsOpenVDisk::Compact, base.ivdsopenvdisk_compact, vds/IVdsOpenVDisk::Compact
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsOpenVDisk.Compact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsOpenVDisk::Compact


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Compacts the virtual disk to reduce the physical size of the backing file.


## -parameters




### -param Flags [in]

A <b>COMPACT_VIRTUAL_DISK_FLAG</b> enumeration value that specifies how the virtual disk is to be compacted. Must be set to COMPACT_VIRTUAL_DISK_FLAG_NONE.


### -param Reserved [in]

This parameter is reserved for system use.


### -param ppAsync [out]

A pointer to an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they have finished with it.  If the <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> method is called on the interface and a success HRESULT value is returned, the interfaces returned in the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://msdn.microsoft.com/en-us/library/ms687197(v=VS.85).aspx">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/en-us/library/ms693474(v=VS.85).aspx">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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



A virtual disk can be compacted only if it is in one of the following states:

<ul>
<li>Detached (offline mode)</li>
<li>Attached and opened with read-only access (online mode)</li>
</ul>
If it is in any other state, the compact operation fails.

The virtual disk must be an expandable (also called dynamic) or differencing virtual disk.

The operation can be safely interrupted and re-run later. If the operation is interrupted and the backing file is reopened, the file's size may be reduced when the file is opened.

The operation can be CPU-intensive or I/O-intensive, or both, depending on how large the virtual disk is and how many unused blocks require manipulation.

This method reduces the size of the virtual disk's backing store file by reclaiming unused space. If this method is called for a virtual disk that is detached, it can only reclaim space in the file that was never used to write data. If it is called for a virtual disk that is attached and opened with read-only access, it is able to reclaim space that was once used, but was later freed. Calling this method for a virtual disk that is attached and opened with read-only access reclaims the maximum amount of free space in the backing store file.




## -see-also




<a href="https://msdn.microsoft.com/3d5f080f-3e83-437e-8cbc-9730988f5dcc">IVdsOpenVDisk</a>
 

 

