---
UID: NF:vdshwprv.IVdsAsync.QueryStatus
title: IVdsAsync::QueryStatus (vdshwprv.h)
description: The IVdsAsync::QueryStatus method (vdshwprv.h) returns when the asynchronous operation is in progress, has finished successfully, or has failed.
helpviewer_keywords: ["IVdsAsync interface [VDS]","QueryStatus method","IVdsAsync.QueryStatus","IVdsAsync::QueryStatus","QueryStatus","QueryStatus method [VDS]","QueryStatus method [VDS]","IVdsAsync interface","base.ivdsasync_querystatus","vds/IVdsAsync::QueryStatus","vdshwprv/IVdsAsync::QueryStatus"]
old-location: base\ivdsasync_querystatus.htm
tech.root: base
ms.assetid: 993228ae-4817-4d88-8544-9cd57cbe8b49
ms.date: 08/08/2022
ms.keywords: IVdsAsync interface [VDS],QueryStatus method, IVdsAsync.QueryStatus, IVdsAsync::QueryStatus, QueryStatus, QueryStatus method [VDS], QueryStatus method [VDS],IVdsAsync interface, base.ivdsasync_querystatus, vds/IVdsAsync::QueryStatus, vdshwprv/IVdsAsync::QueryStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsAsync::QueryStatus
 - vdshwprv/IVdsAsync::QueryStatus
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
 - IVdsAsync.QueryStatus
---

# IVdsAsync::QueryStatus


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

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

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>
