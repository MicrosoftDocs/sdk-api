---
UID: NN:comsvcs.ISystemAppEventData
title: ISystemAppEventData (comsvcs.h)
description: Notifies the subscriber when a COM+ application instance is created or reconfigured.
helpviewer_keywords: ["ISystemAppEventData","ISystemAppEventData interface [COM+]","ISystemAppEventData interface [COM+]","described","_dtc_ISystemAppEventData","comsvcs/ISystemAppEventData","cos.isystemappeventdata"]
old-location: cos\isystemappeventdata.htm
tech.root: cos
ms.assetid: fd88641e-e0ce-44b7-b8b6-59791be48026
ms.date: 12/05/2018
ms.keywords: ISystemAppEventData, ISystemAppEventData interface [COM+], ISystemAppEventData interface [COM+],described, _dtc_ISystemAppEventData, comsvcs/ISystemAppEventData, cos.isystemappeventdata
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISystemAppEventData
 - comsvcs/ISystemAppEventData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISystemAppEventData
---

# ISystemAppEventData interface


## -description

Notifies the subscriber when a COM+ application instance is created or reconfigured. The application event is published to the subscriber by using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISystemAppEventData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISystemAppEventData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISystemAppEventData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isystemappeventdata-ondatachanged">OnDataChanged</a>
</td>
<td align="left" width="63%">
Generated when the configuration of a COM+ application instance is changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-isystemappeventdata-startup">Startup</a>
</td>
<td align="left" width="63%">
Invoked when a COM+ application instance is created.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>