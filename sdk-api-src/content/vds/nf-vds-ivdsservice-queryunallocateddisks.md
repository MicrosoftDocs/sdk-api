---
UID: NF:vds.IVdsService.QueryUnallocatedDisks
title: IVdsService::QueryUnallocatedDisks
author: windows-sdk-content
description: Returns an enumeration object containing a list of the unallocated disks managed by VDS.
old-location: base\ivdsservice_queryunallocateddisks.htm
old-project: VDS
ms.assetid: d519c3d0-7c5a-4c0c-bad9-2429490f2212
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsService interface [VDS],QueryUnallocatedDisks method, IVdsService.QueryUnallocatedDisks, IVdsService::QueryUnallocatedDisks, QueryUnallocatedDisks, QueryUnallocatedDisks method [VDS], QueryUnallocatedDisks method [VDS],IVdsService interface, base.ivdsservice_queryunallocateddisks, vds/IVdsService::QueryUnallocatedDisks
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsService.QueryUnallocatedDisks
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsService::QueryUnallocatedDisks


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns an enumeration object containing a list of the unallocated disks managed by VDS.


## -parameters




### -param ppEnum [out]


      The address of an <a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a> interface pointer that can be used to enumerate the disks  as <a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">disk objects</a>. For more information, see <a href="https://msdn.microsoft.com/cb99e9fd-613c-4e38-9e0f-e1a23b72aa07">Working with Enumeration Objects</a>. Callers must release the interface and each of the disk objects when they are no longer needed by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.
     


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The enumeration was returned successfully.

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

        VDS failed to initialize. If an application calls this method before the service finishes initializing, the 
        method is blocked until the initialization completes. If the initialization fails, this error is returned.

</td>
</tr>
</table>
 




## -remarks




    An unallocated disk is not claimed by any 
    provider. It may or may not contain MBR or GPT partition format information. Often it is an uninitialized disk. If the disk status is <b>VDS_DS_ONLINE</b> or <b>VDS_DS_OFFLINE</b>, the disk is unallocated and uninitialized. If it is <b>VDS_DS_UNKNOWN</b>, <b>VDS_DS_NOT_READY</b>, <b>VDS_DS_FAILED</b>, or <b>VDS_DS_MISSING</b>, it is unallocated, but the VDS service cannot determine whether or not it is initialized, possibly because of problems with the disk.

To determine the disk status, see the <b>status</b> member of the <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> or <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structure for the disk.

If the disk status is <b>VDS_DS_ONLINE</b>, the disk can be added to a pack.

If the disk status is <b>VDS_DS_OFFLINE</b>, try to bring the disk online by calling <a href="https://msdn.microsoft.com/b3366bc7-18ca-4a90-b4e7-e6213a7cc002">IVdsDiskOnline::Online</a>. If the call to the <b>Online</b> method succeeds, the disk can be added to a pack. If the call to <b>Online</b> fails, the disk cannot be used.




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>



<a href="https://msdn.microsoft.com/6b081cc8-fe06-427f-b06d-831a1f1fef52">IVdsService</a>
 

 

