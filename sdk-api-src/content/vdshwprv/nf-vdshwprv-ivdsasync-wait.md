---
UID: NF:vdshwprv.IVdsAsync.Wait
title: IVdsAsync::Wait (vdshwprv.h)
description: Returns when the asynchronous operation has either finished successfully or failed.
helpviewer_keywords: ["IVdsAsync interface [VDS]","Wait method","IVdsAsync.Wait","IVdsAsync::Wait","Wait","Wait method [VDS]","Wait method [VDS]","IVdsAsync interface","base.ivdsasync_wait","vds/IVdsAsync::Wait","vdshwprv/IVdsAsync::Wait"]
old-location: base\ivdsasync_wait.htm
tech.root: base
ms.assetid: 1bb30247-efb8-488f-b142-8912c351f5f2
ms.date: 12/05/2018
ms.keywords: IVdsAsync interface [VDS],Wait method, IVdsAsync.Wait, IVdsAsync::Wait, Wait, Wait method [VDS], Wait method [VDS],IVdsAsync interface, base.ivdsasync_wait, vds/IVdsAsync::Wait, vdshwprv/IVdsAsync::Wait
f1_keywords:
- vdshwprv/IVdsAsync.Wait
dev_langs:
- c++
req.header: vdshwprv.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsAsync::Wait


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns when the asynchronous 
   operation has either finished successfully or failed.


## -parameters




### -param pHrResult [out]

The address of an <b>HRESULT</b> passed in by the caller.


### -param pAsyncOut [out]

The address of a <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a> structure 
      passed in by the caller.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used.

There are two <b>HRESULT</b> return values to examine. The one returned by the method 
       reports failures from the call. The <b>HRESULT</b> returned through 
       <i>pHrResult</i> is used to report failures with the asynchronous operation associated with 
       the <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> object. Both values must be examined.




## -remarks



This method adds a reference to the contained object produced by the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-breakplex">IVdsVolume::BreakPlex</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a>, and 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a>, and 
    <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdscreatepartitionex-createpartitionex">IVdsCreatePartitionEx::CreatePartitionEx</a> 
    methods. Callers must release the reference to the contained object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslun-removeplex">IVdsLun::RemovePlex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolume-breakplex">IVdsVolume::BreakPlex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_async_output">VDS_ASYNC_OUTPUT</a>
 

 

