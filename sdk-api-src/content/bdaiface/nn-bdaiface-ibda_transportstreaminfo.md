---
UID: NN:bdaiface.IBDA_TransportStreamInfo
title: IBDA_TransportStreamInfo
author: windows-sdk-content
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IBDA_TransportStreamInfo interface returns the time when the most recent Program Association Table (PAT) section was received.
old-location: mstv\ibda_transportstreaminfo.htm
tech.root: mstv
ms.assetid: c5f37790-f276-41a5-b5bd-7d8c7a7f587f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_TransportStreamInfo, IBDA_TransportStreamInfo interface [Microsoft TV Technologies], IBDA_TransportStreamInfo interface [Microsoft TV Technologies],described, IBDA_TransportStreamInfoInterface, bdaiface/IBDA_TransportStreamInfo, mstv.ibda_transportstreaminfo
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_TransportStreamInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_TransportStreamInfo interface


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>


The <b>IBDA_TransportStreamInfo</b> interface returns the time when the most recent Program Association Table (PAT) section was received. The <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> implements this interface and registers it as a graph service. To obtain a pointer to this interface, call <b>IServiceProvider::QueryService</b> with the service identifier <b>SID_BDA_TransportStreamInfo</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_TransportStreamInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_TransportStreamInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_TransportStreamInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693460(v=VS.85).aspx">get_PatTableTickCount</a>
</td>
<td align="left" width="63%">
Returns the time when the most recent PAT section was received.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_TransportStreamInfo)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

