---
UID: NF:mfidl.IMFSourceOpenMonitor.OnSourceEvent
title: IMFSourceOpenMonitor::OnSourceEvent (mfidl.h)
description: Called by the network source when the open operation begins or ends.
helpviewer_keywords: ["19b9a891-5116-41b3-8750-85f2c23d3d7f","IMFSourceOpenMonitor interface [Media Foundation]","OnSourceEvent method","IMFSourceOpenMonitor.OnSourceEvent","IMFSourceOpenMonitor::OnSourceEvent","OnSourceEvent","OnSourceEvent method [Media Foundation]","OnSourceEvent method [Media Foundation]","IMFSourceOpenMonitor interface","mf.imfsourceopenmonitor_onsourceevent","mfidl/IMFSourceOpenMonitor::OnSourceEvent"]
old-location: mf\imfsourceopenmonitor_onsourceevent.htm
tech.root: mf
ms.assetid: 19b9a891-5116-41b3-8750-85f2c23d3d7f
ms.date: 12/05/2018
ms.keywords: 19b9a891-5116-41b3-8750-85f2c23d3d7f, IMFSourceOpenMonitor interface [Media Foundation],OnSourceEvent method, IMFSourceOpenMonitor.OnSourceEvent, IMFSourceOpenMonitor::OnSourceEvent, OnSourceEvent, OnSourceEvent method [Media Foundation], OnSourceEvent method [Media Foundation],IMFSourceOpenMonitor interface, mf.imfsourceopenmonitor_onsourceevent, mfidl/IMFSourceOpenMonitor::OnSourceEvent
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSourceOpenMonitor::OnSourceEvent
 - mfidl/IMFSourceOpenMonitor::OnSourceEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceOpenMonitor.OnSourceEvent
---

# IMFSourceOpenMonitor::OnSourceEvent


## -description

Called by the network source when the open operation begins or ends.

## -parameters

### -param pEvent [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The networks source calls this method with the following event types.

<ul>
<li>

<a href="/windows/desktop/medfound/meconnectstart">MEConnectStart</a>


</li>
<li>

<a href="/windows/desktop/medfound/meconnectend">MEConnectEnd</a>


</li>
</ul>
For more information, see <a href="/windows/desktop/medfound/how-to-get-events-from-the-network-source">How to Get Events from the Network Source</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor">IMFSourceOpenMonitor</a>