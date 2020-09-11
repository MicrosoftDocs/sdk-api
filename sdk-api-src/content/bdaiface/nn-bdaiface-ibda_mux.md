---
UID: NN:bdaiface.IBDA_MUX
title: IBDA_MUX (bdaiface.h)
description: Provides access to a device's Mux Service. The Mux Service is used to specify which packet identifiers (PIDs) in the MPEG transport stream are delivered to a media sink device (MSD).
helpviewer_keywords: ["IBDA_MUX","IBDA_MUX interface [Microsoft TV Technologies]","IBDA_MUX interface [Microsoft TV Technologies]","described","bdaiface/IBDA_MUX","mstv.ibda_mux"]
old-location: mstv\ibda_mux.htm
tech.root: mstv
ms.assetid: 5dde7b14-d5a4-4db5-b91f-d6bfd4be269d
ms.date: 12/05/2018
ms.keywords: IBDA_MUX, IBDA_MUX interface [Microsoft TV Technologies], IBDA_MUX interface [Microsoft TV Technologies],described, bdaiface/IBDA_MUX, mstv.ibda_mux
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_MUX
 - bdaiface/IBDA_MUX
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
 - IBDA_MUX
---

# IBDA_MUX interface


## -description

Provides access to a device's Mux Service. The Mux Service is used to specify which packet identifiers (PIDs) in the MPEG transport stream are delivered to a media sink device (MSD).

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_MUX</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_MUX</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_MUX</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_mux-getpidlist">GetPidList</a>
</td>
<td align="left" width="63%">
Gets the list of packet PIDs that are enabled to go across the Protected Broadcast Driver Architecture (PBDA) interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_mux-setpidlist">SetPidList</a>
</td>
<td align="left" width="63%">
Sets the list of PIDs that are enabled to go across the PBDA interface.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_MUX)</code>.

