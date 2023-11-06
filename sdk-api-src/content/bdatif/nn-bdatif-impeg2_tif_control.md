---
UID: NN:bdatif.IMPEG2_TIF_CONTROL
title: IMPEG2_TIF_CONTROL (bdatif.h)
description: IMPEG2_TIF_CONTROL is no longer available for use.
helpviewer_keywords: ["IMPEG2_TIF_CONTROL","IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies]","described","IMPEG2_TIF_CONTROLInterface","bdatif/IMPEG2_TIF_CONTROL","mstv.impeg2_tif_control"]
old-location: mstv\impeg2_tif_control.htm
tech.root: mstv
ms.assetid: 9583365d-b318-49e2-a32f-f6cc9d3f289d
ms.date: 12/05/2018
ms.keywords: IMPEG2_TIF_CONTROL, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies], IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],described, IMPEG2_TIF_CONTROLInterface, bdatif/IMPEG2_TIF_CONTROL, mstv.impeg2_tif_control
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMPEG2_TIF_CONTROL
 - bdatif/IMPEG2_TIF_CONTROL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IMPEG2_TIF_CONTROL
---

# IMPEG2_TIF_CONTROL interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<b>IMPEG2_TIF_CONTROL</b> is no longer available for use. Instead, use the <a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ibda_tif_registration">IBDA_TIF_REGISTRATION</a> interface to register the TIF with the Network Provider, and use the <a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap</a> interface to map or unmap PIDs.]

The <b>IMPEG2_TIF_CONTROL</b> interface is implemented by the <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a>. A Transport Information Filter (TIF) can use this interface to register itself and request table sections carried on specific PIDs within the transport stream. The Network Provider Filter instructs the <a href="/windows/desktop/DirectShow/mpeg-2-demultiplexer">MPEG-2 Demultiplexer</a> (Demux) to send or stop sending the specified packets to the TIF's input pin. All sections are delivered by the Demux to the TIF as complete MPEG-2 table sections.

## -inheritance

The <b>IMPEG2_TIF_CONTROL</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMPEG2_TIF_CONTROL</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2_TIF_CONTROL)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
