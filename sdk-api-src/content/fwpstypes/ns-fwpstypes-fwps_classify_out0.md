---
UID: NS:fwpstypes.FWPS_CLASSIFY_OUT0_
title: FWPS_CLASSIFY_OUT0 (fwpstypes.h)
description: The FWPS_CLASSIFY_OUT0 structure defines the data that is returned to the caller of a callout's classifyFn callout function.Note  FWPS_CLASSIFY_OUT0 is a specific version of FWPS_CLASSIFY_OUT.
helpviewer_keywords: ["FWPS_CLASSIFY_OUT0","FWPS_CLASSIFY_OUT0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_CLASSIFY_OUT0","netvista.fwps_classify_out0","wfp_ref_3_struct_3_fwps_A-E_05656990-cf7c-4fef-a192-88f96860aa02.xml"]
old-location: netvista\fwps_classify_out0.htm
tech.root: NetVista
ms.assetid: 18d84523-bd4c-4f5d-87c7-6fcdcaad6c5d
ms.date: 12/05/2018
ms.keywords: FWPS_CLASSIFY_OUT0, FWPS_CLASSIFY_OUT0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_CLASSIFY_OUT0, netvista.fwps_classify_out0, wfp_ref_3_struct_3_fwps_A-E_05656990-cf7c-4fef-a192-88f96860aa02.xml
req.header: fwpstypes.h
req.include-header: Fwpsk.h, Fwpmtypes.h, Fwpmk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
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
targetos: Windows
req.typenames: FWPS_CLASSIFY_OUT0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_CLASSIFY_OUT0_
 - fwpstypes/FWPS_CLASSIFY_OUT0_
 - FWPS_CLASSIFY_OUT0
 - fwpstypes/FWPS_CLASSIFY_OUT0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpstypes.h
api_name:
 - FWPS_CLASSIFY_OUT0
---

# FWPS_CLASSIFY_OUT0 structure


## -description

The <b>FWPS_CLASSIFY_OUT0</b> structure defines the data that is returned to the caller of a callout's 
  <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function.
<div class="alert"><b>Note</b>  <b>FWPS_CLASSIFY_OUT0</b> is a specific version of <b>FWPS_CLASSIFY_OUT</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field actionType

An <b>FWP_ACTION_TYPE</b> value that specifies the suggested action to be taken as determined by the
     callout driver's 
     <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function. A callout driver
     sets this variable to one of the following values:
     





#### FWP_ACTION_BLOCK

Block the data from being transmitted or received.



#### FWP_ACTION_CONTINUE

Pass the decision to block or permit the data to be transmitted or received to the next filter
       in the filter engine.



#### FWP_ACTION_NONE

Perform no action on the data.



#### FWP_ACTION_NONE_NO_MATCH

Perform no action on the data because it does not match the enumerated filter data types.



#### FWP_ACTION_PERMIT

Permit the data to be transmitted or received.

Write access to this member is controlled by the <b>FWPS_RIGHT_ACTION_WRITE</b> flag in the 
     <b>rights</b> member. If the <b>FWPS_RIGHT_ACTION_WRITE</b> flag is set, a callout driver can write any of the
     above values to this member. If the <b>FWPS_RIGHT_ACTION_WRITE</b> flag is not set, a callout driver should not
     write to this member unless it is vetoing an <b>FWP_ACTION_PERMIT</b> action that was previously returned by a
     higher weight filter in the filter engine. In such a situation, a callout driver sets this member to
     <b>FWP_ACTION_BLOCK</b>.

### -field outContext

Reserved for system use. Callout drivers must not use this member.

### -field filterId

Reserved for system use. Callout drivers must not use this member.

### -field rights

Flags that control the write access to the other members within this structure. Possible flags
     are:
     





#### FWPS_RIGHT_ACTION_WRITE

If this flag is set, a callout driver can write to the 
       <b>actionType</b> member of this structure. If this flag is not set, a callout driver can write only to
       the 
       <b>actionType</b> member of this structure if it is vetoing an <b>FWP_ACTION_PERMIT</b> action that was
       previously returned by a higher weight filter in the filter engine.

### -field flags

Flags that affect the action taken on the data. Possible flags are:
     





#### FWPS_CLASSIFY_OUT_FLAG_ABSORB

The blocked data is to be silently dropped without any event logging or auditing. This is
       typically used for packet modification where the original packet is to be absorbed and the modified
       packet is to be further processed.
       

This flag is applicable at the following layers when the 
       <b>actionType</b> member is set to <b>FWP_ACTION_BLOCK</b>:<dl>
<dd>FWPS_LAYER_INBOUND_MAC_FRAME_NATIVE</dd>
<dd>FWPS_LAYER_OUTBOUND_MAC_FRAME_NATIVE</dd>
<dd>FWPS_LAYER_INBOUND_MAC_FRAME_ETHERNET</dd>
<dd>FWPS_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</dd>
<dd>FWPS_LAYER_INGRESS_VSWITCH_ETHERNET</dd>
<dd>FWPS_LAYER_EGRESS_VSWITCH_ETHERNET</dd>
<dd>FWPS_LAYER_INBOUND_IPPACKET_V4</dd>
<dd>FWPS_LAYER_INBOUND_IPPACKET_V6</dd>
<dd>FWPS_LAYER_OUTBOUND_IPPACKET_V4</dd>
<dd>FWPS_LAYER_OUTBOUND_IPPACKET_V6</dd>
<dd>FWPS_LAYER_INBOUND_TRANSPORT_V4</dd>
<dd>FWPS_LAYER_INBOUND_TRANSPORT_V6</dd>
<dd>FWPS_LAYER_OUTBOUND_TRANSPORT_V4</dd>
<dd>FWPS_LAYER_OUTBOUND_TRANSPORT_V6</dd>
<dd>FWPS_LAYER_INBOUND_ICMP_ERROR_V4</dd>
<dd>FWPS_LAYER_INBOUND_ICMP_ERROR_V6</dd>
<dd>FWPS_LAYER_OUTBOUND_ICMP_ERROR_V4</dd>
<dd>FWPS_LAYER_OUTBOUND_ICMP_ERROR_V6</dd>
<dd>FWPS_LAYER_DATAGRAM_DATA_V4</dd>
<dd>FWPS_LAYER_DATAGRAM_DATA_V6</dd>
<dd>FWPS_LAYER_STREAM_PACKET_V4</dd>
<dd>FWPS_LAYER_STREAM_PACKET_V6</dd>
<dd>FWPS_LAYER_ALE_AUTH_RECV_ACCEPT_V4</dd>
<dd>FWPS_LAYER_ALE_AUTH_RECV_ACCEPT_V6</dd>
<dd>FWPS_LAYER_ALE_AUTH_CONNECT_V4</dd>
<dd>FWPS_LAYER_ALE_AUTH_CONNECT_V6</dd>
</dl>


It is also possible to set this flag at the FWPS_LAYER_ALE_FLOW_ESTABLISHED_V4 and FWPS_LAYER_ALE_FLOW_ESTABLISHED_V6 layers. But doing so is not advised, because these layers are intended for associating context with flows.

If this flag is not set, a blocking action will be subject to normal event logging and
       auditing.



#### FWPS_CLASSIFY_OUT_FLAG_BUFFER_LIMIT_REACHED

The filter engine sets this flag when the filter engine's data buffer for stream data is full.
       This can occur if a callout's 
       <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function repeatedly
       requests more data by setting the 
       <b>streamAction</b> member of the 
       <a href="/windows-hardware/drivers/ddi/content/fwpsk/ns-fwpsk-fwps_stream_callout_io_packet0_">FWPS_STREAM_CALLOUT_IO_PACKET0</a> structure to <b>FWPS_STREAM_ACTION_NEED_MORE_DATA</b> until the buffer
       limit is reached. If this flag is set, the callout driver's 
       <i>classifyFn</i> callout function must either
       permit or block all of the stream data.
       

This flag is only applicable at the stream layers.



#### FWPS_CLASSIFY_OUT_FLAG_NO_MORE_DATA

Stream data was requested after the stream had been disconnected.

### -field reserved

Reserved for system use. Callout drivers must not use this member.

## -remarks

The filter engine passes a pointer to an <b>FWPS_CLASSIFY_OUT0</b> structure to a callout's 
    <a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a> callout function. A callout driver
    uses this structure to return data to the caller.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/fwpsk/ns-fwpsk-fwps_stream_callout_io_packet0_">FWPS_STREAM_CALLOUT_IO_PACKET0</a>



<a href="/windows/desktop/FWP/management-filtering-layer-identifiers-">Run-time Filtering Layer Identifiers</a>



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nc-fwpsk-fwps_callout_classify_fn0">classifyFn</a>