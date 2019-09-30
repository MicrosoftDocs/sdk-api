---
UID: NN:tuner.IESIsdbCasResponseEvent
title: IESIsdbCasResponseEvent (tuner.h)
author: windows-sdk-content
description: Implements methods that get information from a Protected Broadcast Driver Architecture (PBDA) IsdbCasResponse event.
old-location: mstv\iesisdbcasresponseevent.htm
tech.root: mstv
ms.assetid: 141c6798-5dca-495e-bdbe-f07e457a3d8a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESIsdbCasResponseEvent, IESIsdbCasResponseEvent interface [DirectShow], IESIsdbCasResponseEvent interface [DirectShow],described, mstv.iesisdbcasresponseevent, tuner/IESIsdbCasResponseEvent
ms.topic: interface
f1_keywords: 
 - "tuner/IESIsdbCasResponseEvent"
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IESIsdbCasResponseEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESIsdbCasResponseEvent interface


## -description


Implements methods that get information from a Protected Broadcast Driver Architecture (PBDA) <b>IsdbCasResponse</b> event. An Integrated Services Digital Broadcasting (ISDB) PBDA media transform device (MTD) fires an <b>IsdbCasResponse</b> event after a media sink device (MSD)  calls the <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_isdbconditionalaccess-setisdbcasrequest">IBDA_ISDBConditionalAccess::SetIsdbCasRequest</a> method to indicate communication with a conditional access system (CAS) card. The MTD fires the <b>IsdbCasResponse</b> event to signal that response data is available.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESIsdbCasResponseEvent</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iesevent">IESEvent</a>. <b>IESIsdbCasResponseEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESIsdbCasResponseEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesisdbcasresponseevent-getdatalength">GetDataLength</a>
</td>
<td align="left" width="63%">
Gets the length of the response data from the response.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesisdbcasresponseevent-getrequestid">GetRequestId</a>
</td>
<td align="left" width="63%">
Gets the request identifier for the MSD that originated the CAS request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesisdbcasresponseevent-getresponsedata">GetResponseData</a>
</td>
<td align="left" width="63%">
Gets the response data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesisdbcasresponseevent-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Gets the status code from the response.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESIsdbCasResponseEvent)</code>.



