---
UID: NF:vds.IVdsAsync.QueryStatus
title: IVdsAsync::QueryStatus (vds.h)
author: windows-sdk-content
description: Returns when the asynchronous operation is in progress, or has either finished successfully or failed.
old-location: base\ivdsasync_querystatus.htm
tech.root: VDS
ms.assetid: 993228ae-4817-4d88-8544-9cd57cbe8b49
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsAsync interface [VDS],QueryStatus method, IVdsAsync.QueryStatus, IVdsAsync::QueryStatus, QueryStatus, QueryStatus method [VDS], QueryStatus method [VDS],IVdsAsync interface, base.ivdsasync_querystatus, vds/IVdsAsync::QueryStatus, vdshwprv/IVdsAsync::QueryStatus
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
 - IVdsAsync.QueryStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsAsync::QueryStatus


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns when the 
   asynchronous operation is in progress, or has either finished successfully or failed.


## -parameters




### -param pHrResult [out]

The address of an <b>HRESULT</b> for the asynchronous operation passed in by the 
      caller. If the operation is in progress, the value is <b>VDS_E_OPERATION_PENDING</b>. If the 
      operation has finished, the value is the returned <b>HRESULT</b> of the operation.


### -param pulPercentCompleted [out]

The address of a <b>ULONG</b> passed in by the caller, representing the status of the 
      asynchronous operation, given as a percentage. If the operation is in progress, the value is between 0 and 99. 
      If the operation has finished, the value is 100. If the progress of the operation cannot be estimated, the value 
      is 0.


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
The operation is in progress or has completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OPERATION_PENDING</b></dt>
<dt>0x80042409L</dt>
</dl>
</td>
<td width="60%">
The operation is in progress.

</td>
</tr>
</table>
 




## -remarks



The <b>QueryStatus</b> method does not wait for 
    the operation to complete before returning.




## -see-also




<a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a>
 

 

