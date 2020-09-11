---
UID: NN:mfidl.IMFQualityManager
title: IMFQualityManager (mfidl.h)
description: Adjusts playback quality. This interface is exposed by the quality manager.
helpviewer_keywords: ["66781a1f-7469-4222-9e99-6b1415830f4c","IMFQualityManager","IMFQualityManager interface [Media Foundation]","IMFQualityManager interface [Media Foundation]","described","mf.imfqualitymanager","mfidl/IMFQualityManager"]
old-location: mf\imfqualitymanager.htm
tech.root: mf
ms.assetid: 66781a1f-7469-4222-9e99-6b1415830f4c
ms.date: 12/05/2018
ms.keywords: 66781a1f-7469-4222-9e99-6b1415830f4c, IMFQualityManager, IMFQualityManager interface [Media Foundation], IMFQualityManager interface [Media Foundation],described, mf.imfqualitymanager, mfidl/IMFQualityManager
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
 - IMFQualityManager
 - mfidl/IMFQualityManager
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
 - IMFQualityManager
---

# IMFQualityManager interface


## -description

Adjusts playback quality. This interface is exposed by the quality manager.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFQualityManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFQualityManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFQualityManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifypresentationclock">NotifyPresentationClock</a>
</td>
<td align="left" width="63%">
Called when the Media Session selects a presentation clock.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput">NotifyProcessInput</a>
</td>
<td align="left" width="63%">
Called when the media processor is about to deliver an input sample to a pipeline component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput">NotifyProcessOutput</a>
</td>
<td align="left" width="63%">
Called after the media processor gets an output sample from a pipeline component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent">NotifyQualityEvent</a>
</td>
<td align="left" width="63%">
Called when a pipeline component sends an <a href="https://docs.microsoft.com/windows/desktop/medfound/mequalitynotify">MEQualityNotify</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifytopology">NotifyTopology</a>
</td>
<td align="left" width="63%">
Called when the Media Session is about to start playing a new topology.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Called when the Media Session is shutting down.

</td>
</tr>
</table>

## -remarks

Media Foundation provides a default quality manager that is tuned for playback. Applications can provide a custom quality manager to the Media Session by setting the <a href="https://docs.microsoft.com/windows/desktop/medfound/mf-session-quality-manager-attribute">MF_SESSION_QUALITY_MANAGER</a> attribute when creating the Media Session.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

