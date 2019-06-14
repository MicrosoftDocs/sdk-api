---
UID: NN:bdatif.IMPEG2_TIF_CONTROL
title: IMPEG2_TIF_CONTROL (bdatif.h)
author: windows-sdk-content
description: IMPEG2_TIF_CONTROL is no longer available for use.
old-location: mstv\impeg2_tif_control.htm
tech.root: mstv
ms.assetid: 9583365d-b318-49e2-a32f-f6cc9d3f289d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMPEG2_TIF_CONTROL, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies], IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],described, IMPEG2_TIF_CONTROLInterface, bdatif/IMPEG2_TIF_CONTROL, mstv.impeg2_tif_control
ms.topic: interface
req.header: bdatif.h
req.include-header: 
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
 - Bdatif.h
api_name:
 - IMPEG2_TIF_CONTROL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMPEG2_TIF_CONTROL interface


## -description


<p class="CCE_Message">[<b>IMPEG2_TIF_CONTROL</b> is no longer available for use. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ibda_tif_registration">IBDA_TIF_REGISTRATION</a> interface to register the TIF with the Network Provider, and use the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap</a> interface to map or unmap PIDs.]

The <b>IMPEG2_TIF_CONTROL</b> interface is implemented by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a>. A Transport Information Filter (TIF) can use this interface to register itself and request table sections carried on specific PIDs within the transport stream. The Network Provider Filter instructs the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> (Demux) to send or stop sending the specified packets to the TIF's input pin. All sections are delivered by the Demux to the TIF as complete MPEG-2 table sections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2_TIF_CONTROL</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMPEG2_TIF_CONTROL</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2_TIF_CONTROL</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-addpids">AddPIDs</a>
</td>
<td align="left" width="63%">
Notifies the Network Provider which PIDs the TIF should receive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-deletepids">DeletePIDs</a>
</td>
<td align="left" width="63%">
Informs the Network Provider that the TIF no longer requires the specified PID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-getpidcount">GetPIDCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of MPEG-2 Packet IDs being filtered by the Demux into the TIF's input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-getpids">GetPIDs</a>
</td>
<td align="left" width="63%">
Retrieves the list of MPEG-2 Packet IDs being filtered into the TIF's input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-registertif">RegisterTIF</a>
</td>
<td align="left" width="63%">
Called by the Transport Information Filter to register itself with the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-impeg2_tif_control-unregistertif">UnregisterTIF</a>
</td>
<td align="left" width="63%">
Called by the Transport Information Filter to unregister itself with the Network Provider.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2_TIF_CONTROL)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

