---
UID: NS:ndkinfo._NDK_ADAPTER_INFO
title: NDK_ADAPTER_INFO (ndkinfo.h)
description: The NDK_ADAPTER_INFO structure specifies information about limits and capabilities of an NDK adapter.
helpviewer_keywords: ["NDK_ADAPTER_FLAG_CQ_INTERRUPT_MODERATION_SUPPORTED","NDK_ADAPTER_FLAG_CQ_RESIZE_SUPPORTED","NDK_ADAPTER_FLAG_IN_ORDER_DMA_SUPPORTED","NDK_ADAPTER_FLAG_LOOPBACK_CONNECTIONS_SUPPORTED","NDK_ADAPTER_FLAG_MULTI_ENGINE_SUPPORTED","NDK_ADAPTER_FLAG_RDMA_READ_LOCAL_INVALIDATE_SUPPORTED","NDK_ADAPTER_FLAG_RDMA_READ_SINK_NOT_REQUIRED","NDK_ADAPTER_INFO","NDK_ADAPTER_INFO structure [Network Drivers Starting with Windows Vista]","ndkinfo/NDK_ADAPTER_INFO","netvista.ndk_adapter_info"]
old-location: netvista\ndk_adapter_info.htm
tech.root: NetVista
ms.assetid: 3F8EAA7F-20CE-4948-9F10-E23025B174E7
ms.date: 12/05/2018
ms.keywords: NDK_ADAPTER_FLAG_CQ_INTERRUPT_MODERATION_SUPPORTED, NDK_ADAPTER_FLAG_CQ_RESIZE_SUPPORTED, NDK_ADAPTER_FLAG_IN_ORDER_DMA_SUPPORTED, NDK_ADAPTER_FLAG_LOOPBACK_CONNECTIONS_SUPPORTED, NDK_ADAPTER_FLAG_MULTI_ENGINE_SUPPORTED, NDK_ADAPTER_FLAG_RDMA_READ_LOCAL_INVALIDATE_SUPPORTED, NDK_ADAPTER_FLAG_RDMA_READ_SINK_NOT_REQUIRED, NDK_ADAPTER_INFO, NDK_ADAPTER_INFO structure [Network Drivers Starting with Windows Vista], ndkinfo/NDK_ADAPTER_INFO, netvista.ndk_adapter_info
req.header: ndkinfo.h
req.include-header: Ndkpi.h
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr: Windows Server 2012
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
targetos: Windows
req.typenames: NDK_ADAPTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NDK_ADAPTER_INFO
 - ndkinfo/_NDK_ADAPTER_INFO
 - NDK_ADAPTER_INFO
 - ndkinfo/NDK_ADAPTER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndkinfo.h
api_name:
 - NDK_ADAPTER_INFO
---

# NDK_ADAPTER_INFO structure


## -description

The <b>NDK_ADAPTER_INFO</b> structure specifies information about limits and capabilities of an NDK adapter.

## -struct-fields

### -field Version

The  major and minor versions of the NDK interface (<a href="/windows/desktop/api/ndkinfo/ns-ndkinfo-ndk_version">NDK_VERSION</a>).

### -field VendorId

A vendor's organizational unique identifier (OUI).

### -field DeviceId

A vendor defined device identifier.

### -field MaxRegistrationSize

The maximum size, in bytes, of a single memory registration that the adapter can address.

### -field MaxWindowSize

The maximum size, in bytes, for a single memory window.

### -field FRMRPageCount

The fast-register memory region (FRMR) size (in <b>PAGE_SIZE</b> pages) for which the adapter supports the greatest number of FRMRs. A provider must support at least 16 FRMR pages. This value is typically used by upper layers as an FRMR size that optimizes concurrent FRMR-based I/O operations. Hence, advertising a value greater than 16 should be done only if the total number of FRMRs supported with that size is not meaningfully reduced as a result.

### -field MaxInitiatorRequestSge

The maximum number of scatter-gather entries (SGEs) that can be specified in a single request over an initiator queue.

### -field MaxReceiveRequestSge

The maximum number of SGEs that can be specified in a single request over a receive queue.

### -field MaxReadRequestSge

The maximum number of SGEs that can be specified in a read request. 

<div class="alert"><b>Note</b>  This  value overrides the <b>MaxInitiatorRequestSge</b> value for read requests.</div>
<div> </div>

### -field MaxTransferLength

The maximum total length that can be referenced by all SGEs in a single send, receive, read, or write request.

### -field MaxInlineDataSize

The maximum amount of inline data, in bytes, that can be sent in a single send or write request.

### -field MaxInboundReadLimit

The maximum number of in-progress incoming read operations for each QP.

### -field MaxOutboundReadLimit

The maximum number of in-progress outgoing read operations for each QP.

### -field MaxReceiveQueueDepth

The maximum number of outstanding requests for each receive queue.

### -field MaxInitiatorQueueDepth

The maximum number of outstanding requests for each initiator queue.

### -field MaxSrqDepth

The maximum number of outstanding requests for each shared receive queue (SRQ). A value of zero means no SRQ support.

### -field MaxCqDepth

The maximum number of completion entries for each completion queue (CQ).

### -field LargeRequestThreshold

The data size hint, in bytes, above which read and write operations will yield better results than send and receive operations.

### -field MaxCallerData

 The maximum size, in bytes, of the private data that can be sent with a 
    connect request.

### -field MaxCalleeData

The maximum size, in bytes, of the private data that can be sent with an accept or reject request.

### -field AdapterFlags

A set of  flags that determine adapter properties. The currently defined flags include:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_IN_ORDER_DMA_SUPPORTED"></a><a id="ndk_adapter_flag_in_order_dma_supported"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_IN_ORDER_DMA_SUPPORTED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set if the provider writes incoming data into the consumer’s buffer in order. That is, the last byte position in the consumer’s buffer is guaranteed not to be updated before any prior byte position.

</td>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_RDMA_READ_SINK_NOT_REQUIRED"></a><a id="ndk_adapter_flag_rdma_read_sink_not_required"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_RDMA_READ_SINK_NOT_REQUIRED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
 

Set if the provider does not require special access rights on the sink buffer for an RDMA read request. When this flag is set, the consumer is not required to use the NDK_MR_FLAG_RDMA_READ_SINK or NDK_OP_FLAG_RDMA_READ_SINK flags when it registers sink buffers for RDMA read requests.  The consumer can also use logical address mappings directly (with a token obtained with the  <a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_get_privileged_memory_region_token">NDK_FN_GET_PRIVILEGED_MEMORY_REGION_TOKEN</a>  function) as RDMA read sink buffers.  This is similar to access to local buffers for RDMA write, send, and receive operations.

</td>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_CQ_INTERRUPT_MODERATION_SUPPORTED"></a><a id="ndk_adapter_flag_cq_interrupt_moderation_supported"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_CQ_INTERRUPT_MODERATION_SUPPORTED</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Set if the provider supports programmatically controlled interrupt moderation for each completion queue (CQ). When this flag is set, an NDK consumer can use the <a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_control_cq_interrupt_moderation">NDK_FN_CONTROL_CQ_INTERRUPT_MODERATION</a> function in the <a href="/windows-hardware/drivers/ddi/content/ndkpi/ns-ndkpi-_ndk_cq_dispatch">NDK_CQ_DISPATCH</a> table.

</td>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_MULTI_ENGINE_SUPPORTED"></a><a id="ndk_adapter_flag_multi_engine_supported"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_MULTI_ENGINE_SUPPORTED</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Set if the provider supports concurrent processing of multiple connections with multiple execution engines. If this flag is set,  an NDK consumer that uses more than one connection concurrently on the adapter might provide better performance than a single connection.

</td>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_RDMA_READ_LOCAL_INVALIDATE_SUPPORTED"></a><a id="ndk_adapter_flag_rdma_read_local_invalidate_supported"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_RDMA_READ_LOCAL_INVALIDATE_SUPPORTED</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Set if the provider supports invalidation of the local token specified in the first <a href="/windows-hardware/drivers/ddi/content/ndkpi/ns-ndkpi-_ndk_sge">NDK_SGE</a> passed to an <i>NdkRead</i> (<a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_read">NDK_FN_READ</a>) function when completing the read request.

<b>Note</b>  This value is supported only in NDKPI 1.2 (Windows Server 2012 R2) and later.

</td>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_CQ_RESIZE_SUPPORTED"></a><a id="ndk_adapter_flag_cq_resize_supported"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_CQ_RESIZE_SUPPORTED</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Set if the provider supports resizing CQ objects. If this flag is not set,  the consumer must not attempt a   CQ resize.

</td>
</tr>
<tr>
<td width="40%"><a id="NDK_ADAPTER_FLAG_LOOPBACK_CONNECTIONS_SUPPORTED"></a><a id="ndk_adapter_flag_loopback_connections_supported"></a><dl>
<dt><b>NDK_ADAPTER_FLAG_LOOPBACK_CONNECTIONS_SUPPORTED</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Set if the provider supports loopback connections. That is, loopback  from a local network address on a given RNIC to the same local address on the same RNIC.

</td>
</tr>
</table>

### -field RdmaTechnology

## -remarks

The <a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_query_adapter_info">NDK_FN_QUERY_ADAPTER_INFO</a> function retrieves the <b>NDK_ADAPTER_INFO</b>, which contains information on various limits and capabilities of the adapter.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ndkpi/ns-ndkpi-_ndk_cq_dispatch">NDK_CQ_DISPATCH</a>



<a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_control_cq_interrupt_moderation">NDK_FN_CONTROL_CQ_INTERRUPT_MODERATION</a>



<a href="/windows-hardware/drivers/ddi/content/ndkpi/nc-ndkpi-ndk_fn_get_privileged_memory_region_token">NDK_FN_GET_PRIVILEGED_MEMORY_REGION_TOKEN</a>



<a href="/windows/desktop/api/ndkinfo/ns-ndkinfo-ndk_version">NDK_VERSION</a>