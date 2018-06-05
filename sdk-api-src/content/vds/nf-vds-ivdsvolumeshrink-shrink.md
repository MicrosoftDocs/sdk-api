---
UID: NF:vds.IVdsVolumeShrink.Shrink
title: IVdsVolumeShrink::Shrink
author: windows-sdk-content
description: Shrinks the volume and all plexes and returns the released extents.
old-location: base\ivdsvolumeshrink_shrink.htm
old-project: VDS
ms.assetid: a6d91cb0-b9a4-4a5f-94bc-824b1691bcd7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsVolumeShrink interface,Shrink method, IVdsVolumeShrink.Shrink, IVdsVolumeShrink::Shrink, Shrink, Shrink method, Shrink method,IVdsVolumeShrink interface, base.ivdsvolumeshrink_shrink, vds/IVdsVolumeShrink::Shrink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
-	IVdsVolumeShrink.Shrink
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVolumeShrink::Shrink


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Shrinks the volume and all plexes and returns the released extents.


## -parameters




### -param ullDesiredNumberOfReclaimableBytes [in]

Maximum number of bytes by which to shrink the size of the volume. The value of this parameter must be greater than or equal to the value of the <i>ullMinNumberOfReclaimableBytes</i> parameter.  If the number of bytes specified is not a multiple of the file system cluster size, the <b>Shrink</b> method will round this value up to the next multiple of the file system cluster size.


### -param ullMinNumberOfReclaimableBytes [in]

Minimum number of bytes by which to shrink the size of the volume.  If the volume size cannot be shrunk by at least this number of bytes, the <b>Shrink</b> method fails.  If the number of bytes specified is not a multiple of the file system cluster size, the <b>Shrink</b> method will round this value up to the next multiple of the file system cluster size.  Specify zero to indicate that no minimum number of reclaimable bytes is required for the <b>Shrink</b> method to succeed.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait for, 
      or query the status of the operation. If 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> is called and a success HRESULT value is returned, the interfaces returned in 
      the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="_com_succeeded">SUCCEEDED</a> and <a href="_com_failed">FAILED</a> macros defined in Winerror.h.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANNOT_SHRINK</b></dt>
<dt>0x8004251EL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be shrunk because the file system does not support it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DISK_REMOVEABLE</b></dt>
<dt>0x8004255AL</dt>
</dl>
</td>
<td width="60%">
The operation is not supported on removable media.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INTERNAL_ERROR</b></dt>
<dt>0x80042448L</dt>
</dl>
</td>
<td width="60%">
An internal error occurred. Check the event log for more details.

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
No volume arrival notification was received. You may need to call <a href="https://msdn.microsoft.com/ca6a1143-b5f0-49e5-8505-836c565aabcf">IVdsService::Refresh</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_SHRINK_SIZE_TOO_BIG</b></dt>
<dt>0x80042574L</dt>
</dl>
</td>
<td width="60%">
The specified shrink size is too large and will cause the volume to be smaller than the minimum volume size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_SHRINK_SIZE_LESS_THAN_MIN</b></dt>
<dt>0x80042573L</dt>
</dl>
</td>
<td width="60%">
The specified shrink size is less than the minimum shrink size allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_NOT_HEALTHY</b></dt>
<dt>0x8004243EL</dt>
</dl>
</td>
<td width="60%">
The volume is not healthy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_SIMPLE_SPANNED</b></dt>
<dt>0x80042589L</dt>
</dl>
</td>
<td width="60%">
The operation is only supported on simple or spanned volumes.

</td>
</tr>
</table>
 




## -remarks



The <b>Shrink</b> method moves the files so that they are as close as possible to the beginning of the volume, in order to consolidate free space at the end of the volume.  (The amount of free space that can be consolidated at the end of the volume determines how much the volume can be shrunk.) It then truncates the file system volume, reducing its size, and then truncates the partition or dynamic volume.

In almost all cases, there will be some files that are immovable (that is, files that cannot be moved). For example, file system and storage driver metadata files are likely to be immovable. For this reason, the amount by which a volume can be shrunk is usually less than the total amount of free space on the volume.

The number and placement of immovable files can vary from one computer to the next, even if both computers are configured identically.

It is possible for a file to be temporarily immovable. For this reason, an application may be able to recover additional space if it calls this method a second time with the same parameters.

If the <i>ullDesiredNumberOfReclaimableBytes</i> and <i>ullMinNumberOfReclaimableBytes</i> parameters are both zero, the <b>Shrink</b> method will shrink the volume by as much as possible.

Shrink and <a href="https://msdn.microsoft.com/library/windows/hardware/dn922720">extend</a> operations are supported only on NTFS and RAW volumes.

Use this method to shrink the file system and volume. If VDS fails to shrink the volume, it stops the operation without shrinking the file system.

Only one shrink or defragmentation operation can be performed at a time on each volume.<b>Windows Server 2008 and Windows Vista:  </b>Only one shrink or defragmentation operation can be performed at a time on a computer.



Implementers must return a pointer to the <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface for this method, even if the call does not initiate an asynchronous operation.

This method is identical to the <a href="https://msdn.microsoft.com/63ac6ef9-0e84-40ed-a302-4f32316a41cc">IVdsVolume::Shrink</a> method.

You can use the <a href="https://msdn.microsoft.com/416ceb78-50fb-4976-8814-3981b594ebec">IVdsVolumeShrink::QueryMaxReclaimableBytes</a> method to estimate the number of bytes to be reclaimed by the shrink operation. However, <b>QueryMaxReclaimableBytes</b> can return more bytes than are actually available. For more information, see "IVdsVolumeShrink::Shrink fails when provided value returned from QueryMaxReclaimableBytes" in the Help and Support Knowledge Base at <a href="http://go.microsoft.com/fwlink/p/?linkid=167966">http://go.microsoft.com/fwlink/p/?linkid=167966</a>.




## -see-also




<a href="https://msdn.microsoft.com/8f31dd3e-0c06-49fe-8ff2-55cfabe5099e">IVdsVolume::Extend</a>



<a href="https://msdn.microsoft.com/08c354a6-5cc0-405c-91cf-dca55b87b49a">IVdsVolumeShrink</a>
 

 

