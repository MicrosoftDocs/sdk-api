---
UID: NF:vds.IVdsVolume.Shrink
title: IVdsVolume::Shrink
author: windows-sdk-content
description: Reduces the size of the volume and all plexes, and returns the released extents to free space.
old-location: base\ivdsvolume_shrink.htm
tech.root: vds
ms.assetid: 63ac6ef9-0e84-40ed-a302-4f32316a41cc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsVolume interface [VDS],Shrink method, IVdsVolume.Shrink, IVdsVolume::Shrink, Shrink, Shrink method [VDS], Shrink method [VDS],IVdsVolume interface, base.ivdsvolume_shrink, vds/IVdsVolume::Shrink
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
 - IVdsVolume.Shrink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolume::Shrink


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Reduces the size of the volume 
   and all plexes, and returns the released extents to free space. 
   
  


## -parameters




### -param ullNumberOfBytesToRemove [in]

The size of the reduction in bytes.


### -param ppAsync [out]

The address of an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface pointer. VDS 
      initializes the interface on return. Callers must release the interface. Use this interface to cancel, wait for, 
      or query the status of the operation. If 
      <a href="https://msdn.microsoft.com/1bb30247-efb8-488f-b142-8912c351f5f2">IVdsAsync::Wait</a> is called and a success HRESULT value is returned, the interfaces returned in 
      the <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure must be released by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method on each interface pointer. However, if <b>Wait</b> returns a failure HRESULT value, or if the <i>pHrResult</i> parameter of <b>Wait</b> receives a failure HRESULT value, the interface pointers in the <b>VDS_ASYNC_OUTPUT</b> structure are <b>NULL</b> and do not need to be released. You can test for success or failure HRESULT values by using the <a href="https://msdn.microsoft.com/en-us/library/ms687197(v=VS.85).aspx">SUCCEEDED</a> and <a href="https://msdn.microsoft.com/en-us/library/ms693474(v=VS.85).aspx">FAILED</a> macros defined in Winerror.h.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
<dt><b><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a provider 
        that caches information about the attached devices. The caller can use the 
        <a href="https://msdn.microsoft.com/aeb06a98-8896-446f-abd5-ea40be0bea40">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="https://msdn.microsoft.com/25ddc73c-5d1b-4bec-bbc2-9f22a5f82ffe">IVdsHwProvider::Refresh</a> 
        method to restore the cache.
       

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
<dt><b>VDS_E_SHRINK_SIZE_TOO_BIG</b></dt>
<dt>0x80042574L</dt>
</dl>
</td>
<td width="60%">
The specified shrink size is too large and will cause the volume to be smaller than the minimum volume size.

</td>
</tr>
</table>
 




## -remarks



This method is a wrapper for the <a href="https://msdn.microsoft.com/a6d91cb0-b9a4-4a5f-94bc-824b1691bcd7">IVdsVolumeShrink::Shrink</a> method. If you call <b>IVdsVolume::Shrink</b>, the value of the <i>uNumberOfBytesToRemove</i> parameter is used for the <i>ullDesiredNumberOfReclaimableBytes</i> and <i>ullMinNumberOfReclaimableBytes</i> parameters of <b>IVdsVolumeShrink::Shrink</b>.

Shrink and <a href="https://msdn.microsoft.com/8f31dd3e-0c06-49fe-8ff2-55cfabe5099e">extend</a> operations are supported only on NTFS and RAW volumes.

Use this method to shrink the file system and volume. If VDS fails to shrink the volume, it stops the operation 
    without shrinking the file system.
   

Only one shrink or defragmentation operation can be performed at a time on each volume.<b>Windows Server 2008 and Windows Vista:  </b>Only one shrink or defragmentation operation can be performed at a time on a computer.



If <i>uNumberOfBytesToRemove</i> is zero, the method fails. Otherwise, VDS rounds 
    <i>uNumberOfBytesToRemove</i> to a multiple of the file system cluster size.
     
     
      

Implementers must return a pointer to the <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface for 
      this method, even if the call does not initiate an asynchronous operation.

You can use the <a href="https://msdn.microsoft.com/416ceb78-50fb-4976-8814-3981b594ebec">IVdsVolumeShrink::QueryMaxReclaimableBytes</a> method to estimate the number of bytes to be reclaimed by the shrink operation. However, <b>QueryMaxReclaimableBytes</b> can return more bytes than are actually available. For more information, see "IVdsVolumeShrink::Shrink fails when provided value returned from QueryMaxReclaimableBytes" in the Help and Support Knowledge Base at <a href="http://go.microsoft.com/fwlink/p/?linkid=167966">http://go.microsoft.com/fwlink/p/?linkid=167966</a>.




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/a02ee0a6-ac29-406c-9fc0-4f632d32424f">IVdsVolume</a>



<a href="https://msdn.microsoft.com/8f31dd3e-0c06-49fe-8ff2-55cfabe5099e">IVdsVolume::Extend</a>
 

 

