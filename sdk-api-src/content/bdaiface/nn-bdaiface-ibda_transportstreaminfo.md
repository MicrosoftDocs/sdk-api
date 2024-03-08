---
UID: NN:bdaiface.IBDA_TransportStreamInfo
title: IBDA_TransportStreamInfo (bdaiface.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IBDA_TransportStreamInfo interface returns the time when the most recent Program Association Table (PAT) section was received.
helpviewer_keywords: ["IBDA_TransportStreamInfo","IBDA_TransportStreamInfo interface [Microsoft TV Technologies]","IBDA_TransportStreamInfo interface [Microsoft TV Technologies]","described","IBDA_TransportStreamInfoInterface","bdaiface/IBDA_TransportStreamInfo","mstv.ibda_transportstreaminfo"]
old-location: mstv\ibda_transportstreaminfo.htm
tech.root: mstv
ms.assetid: c5f37790-f276-41a5-b5bd-7d8c7a7f587f
ms.date: 12/05/2018
ms.keywords: IBDA_TransportStreamInfo, IBDA_TransportStreamInfo interface [Microsoft TV Technologies], IBDA_TransportStreamInfo interface [Microsoft TV Technologies],described, IBDA_TransportStreamInfoInterface, bdaiface/IBDA_TransportStreamInfo, mstv.ibda_transportstreaminfo
req.header: bdaiface.h
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
 - IBDA_TransportStreamInfo
 - bdaiface/IBDA_TransportStreamInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_TransportStreamInfo
---

# IBDA_TransportStreamInfo interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>


The <b>IBDA_TransportStreamInfo</b> interface returns the time when the most recent Program Association Table (PAT) section was received. The <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> implements this interface and registers it as a graph service. To obtain a pointer to this interface, call <b>IServiceProvider::QueryService</b> with the service identifier <b>SID_BDA_TransportStreamInfo</b>.

## -inheritance

The <b>IBDA_TransportStreamInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_TransportStreamInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_TransportStreamInfo)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
