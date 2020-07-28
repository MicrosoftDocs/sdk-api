---
UID: NF:strmif.IAMDevMemoryControl.WriteSync
title: IAMDevMemoryControl::WriteSync (strmif.h)
description: Note  The IAMDevMemoryControl interface is deprecated. Used to synchronize with the completed write. This method returns when any data being written to the particular allocator region is fully written into the memory.
helpviewer_keywords: ["IAMDevMemoryControl interface [DirectShow]","WriteSync method","IAMDevMemoryControl.WriteSync","IAMDevMemoryControl::WriteSync","IAMDevMemoryControlWriteSync","WriteSync","WriteSync method [DirectShow]","WriteSync method [DirectShow]","IAMDevMemoryControl interface","dshow.iamdevmemorycontrol_writesync","strmif/IAMDevMemoryControl::WriteSync"]
old-location: dshow\iamdevmemorycontrol_writesync.htm
tech.root: dshow
ms.assetid: 46bf7ab6-cc3c-4846-a8f8-97c62ede4aaf
ms.date: 12/05/2018
ms.keywords: IAMDevMemoryControl interface [DirectShow],WriteSync method, IAMDevMemoryControl.WriteSync, IAMDevMemoryControl::WriteSync, IAMDevMemoryControlWriteSync, WriteSync, WriteSync method [DirectShow], WriteSync method [DirectShow],IAMDevMemoryControl interface, dshow.iamdevmemorycontrol_writesync, strmif/IAMDevMemoryControl::WriteSync
f1_keywords:
- strmif/IAMDevMemoryControl.WriteSync
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmif.h
api_name:
- IAMDevMemoryControl.WriteSync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMDevMemoryControl::WriteSync


## -description



<div class="alert"><b>Note</b>  The <b>IAMDevMemoryControl</b> interface is deprecated.</div>
<div> </div>
Used to synchronize with the completed write. This method returns when any data being written to the particular allocator region is fully written into the memory.




## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
A time-out has occurred without this method confirming that data was written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The data was successfully written into memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_COMMITTED</b></dt>
</dl>
</td>
<td width="60%">
The allocator hasn't called the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-imemallocator-commit">IMemAllocator::Commit</a> method.

</td>
</tr>
</table>
 




## -remarks



This method guarantees that all prior write operations to allocated memory have succeeded. Subsequent memory write operations require another call to <code>WriteSync</code>.

This method is implementation dependent, and is used (when necessary) to synchronize memory write operations to the memory. The driver of the on-board memory provides the implementation.

The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdevmemorycontrol">IAMDevMemoryControl</a> interface is typically found on memory that is accessed through a Peripheral Component Interconnect (PCI) bridge. (A PCI is a local bus for personal computers that provides a high-speed data path between the processor and peripheral devices.) Memory behind a PCI bridge must be synchronized after a memory write operation completes, if another device will access that memory from behind the PCI bridge. This is because the host access to the memory is buffered through the PCI bridge FIFO (first in first out), and the host will assume the write is completed before the bridge actually writes the data. A subsequent action by a device behind the bridge, such as a SCSI controller, might read the memory before the write is completed, if the <b>IAMDevMemoryControl::WriteSync</b> method is not called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdevmemorycontrol">IAMDevMemoryControl Interface</a>
 

 

