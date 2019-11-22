---
UID: NN:comsvcs.IMtsEventInfo
title: IMtsEventInfo (comsvcs.h)

description: Describes user-defined events.
old-location: cos\imtseventinfo.htm
tech.root: cossdk
ms.assetid: 9508df6d-281b-4a02-bb95-233b369b8279

ms.date: 12/05/2018
ms.keywords: IMtsEventInfo, IMtsEventInfo interface [COM+], IMtsEventInfo interface [COM+],described, _dtc_IMtsEventInfo_Interface, comsvcs/IMtsEventInfo, cos.imtseventinfo
ms.topic: interface
f1_keywords: 
 - "comsvcs/IMtsEventInfo"
dev_langs:
 - c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ComSvcs.h
api_name:
 - IMtsEventInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMtsEventInfo interface


## -description


Describes user-defined events. The events are published to the subscriber using the <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMtsEventInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMtsEventInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMtsEventInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtseventinfo-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of data values from the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtseventinfo-get_displayname">get_DisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtseventinfo-get_eventid">get_EventID</a>
</td>
<td align="left" width="63%">
Retrieves the event identifier of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtseventinfo-get_names">get_Names</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the names of the data values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imtseventinfo-get_value">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified user-defined event.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
 

 

