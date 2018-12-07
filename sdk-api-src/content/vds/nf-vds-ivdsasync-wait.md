---
UID: NF:vds.IVdsAsync.Wait
title: IVdsAsync::Wait
author: windows-sdk-content
description: Returns when the asynchronous operation has either finished successfully or failed.
old-location: base\ivdsasync_wait.htm
tech.root: vds
ms.assetid: 1bb30247-efb8-488f-b142-8912c351f5f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsAsync interface [VDS],Wait method, IVdsAsync.Wait, IVdsAsync::Wait, Wait, Wait method [VDS], Wait method [VDS],IVdsAsync interface, base.ivdsasync_wait, vds/IVdsAsync::Wait, vdshwprv/IVdsAsync::Wait
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsAsync.Wait
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAsync::Wait


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns when the asynchronous 
   operation has either finished successfully or failed.


## -parameters




### -param pHrResult [out]

The address of an <b>HRESULT</b> passed in by the caller.


### -param pAsyncOut [out]

The address of a <a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a> structure 
      passed in by the caller.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used.

There are two <b>HRESULT</b> return values to examine. The one returned by the method 
       reports failures from the call. The <b>HRESULT</b> returned through 
       <i>pHrResult</i> is used to report failures with the asynchronous operation associated with 
       the <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> object. Both values must be examined.




## -remarks



This method adds a reference to the contained object produced by the 
    <a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>, 
    <a href="https://msdn.microsoft.com/c7e42aa4-3233-40e9-b537-043eecd192ad">IVdsVolume::BreakPlex</a>, 
    <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a>, and 
    <a href="https://msdn.microsoft.com/94f80a9f-459f-4f3d-8d85-e5ec7d5734c4">IVdsAdvancedDisk::CreatePartition</a>, and 
    <a href="https://msdn.microsoft.com/c9ab5a24-b0b3-41cc-a4bf-3619f156008c">IVdsCreatePartitionEx::CreatePartitionEx</a> 
    methods. Callers must release the reference to the contained object.




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>



<a href="https://msdn.microsoft.com/9959c2a3-f282-4512-9d3f-da8842d5ee79">IVdsLun::RemovePlex</a>



<a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>



<a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a>



<a href="https://msdn.microsoft.com/c7e42aa4-3233-40e9-b537-043eecd192ad">IVdsVolume::BreakPlex</a>



<a href="https://msdn.microsoft.com/21771c6a-eca9-47f3-b6fc-383bca1e11bf">VDS_ASYNC_OUTPUT</a>
 

 

