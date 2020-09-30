---
UID: NN:xaudio2.IXAudio2
title: IXAudio2 (xaudio2.h)
description: IXAudio2 is the interface for the XAudio2 object that manages all audio engine states, the audio processing thread, the voice graph, and so forth.
helpviewer_keywords: ["IXAudio2","IXAudio2 Interface","IXAudio2 Interface interface [XAudio2 Audio Mixing APIs]","IXAudio2 Interface interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2","xaudio2/IXAudio2"]
old-location: xaudio2\ixaudio2.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2.IXAudio2
ms.date: 12/05/2018
ms.keywords: IXAudio2, IXAudio2 Interface, IXAudio2 Interface interface [XAudio2 Audio Mixing APIs], IXAudio2 Interface interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2, xaudio2/IXAudio2
req.header: xaudio2.h
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2
 - xaudio2/IXAudio2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2 Interface
---

# IXAudio2 interface


## -description

IXAudio2 is the interface for the <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> object that manages all audio engine states, the audio processing thread, the voice graph, and so forth. 

This is the only XAudio2 interface that is derived from the COM <b>IUnknown</b> interface. It controls the lifetime of the <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> object using two methods derived from <b>IUnknown</b>: <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-addref">IXAudio2::AddRef</a> and <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-release">IXAudio2::Release</a>. No other XAudio2 objects are reference-counted; their lifetimes are explicitly controlled using <i>create</i> and <i>destroy</i> calls, and are bounded by the lifetime of the XAudio2 object that owns them.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXAudio2 Interface</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXAudio2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXAudio2 Interface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-addref">AddRef</a>
</td>
<td align="left" width="63%">
Adds a reference to the XAudio2 object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges">CommitChanges</a>
</td>
<td align="left" width="63%">
Atomically applies a set of operations that are tagged with a given identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice">CreateMasteringVoice</a>
</td>
<td align="left" width="63%">
Creates and configures a mastering voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice">CreateSourceVoice</a>
</td>
<td align="left" width="63%">
Creates and configures a source voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice">CreateSubmixVoice</a>
</td>
<td align="left" width="63%">
Creates and configures a submix voice.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata">GetPerformanceData</a>
</td>
<td align="left" width="63%">
Returns current resource usage details, such as available memory or CPU usage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-queryinterface">QueryInterface</a>
</td>
<td align="left" width="63%">
Queries for a given COM interface on the XAudio2 object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks">RegisterForCallbacks</a>
</td>
<td align="left" width="63%">
Adds an <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> pointer to the <b>XAudio2</b> engine callback list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-release">Release</a>
</td>
<td align="left" width="63%">
Releases a reference to the XAudio2 object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration">SetDebugConfiguration</a>
</td>
<td align="left" width="63%">
Changes global debug logging options for XAudio2.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine">StartEngine</a>
</td>
<td align="left" width="63%">
Starts the audio processing thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-stopengine">StopEngine</a>
</td>
<td align="left" width="63%">
Stops the audio processing thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks">UnregisterForCallbacks</a>
</td>
<td align="left" width="63%">
Removes an <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback">IXAudio2EngineCallback</a> pointer from the <b>XAudio2</b> engine callback list.

</td>
</tr>
</table>

## -remarks

The DirectX SDK versions of XAUDIO2 included three member functions that are not present in the Windows 8 version: <b>GetDeviceCount</b>, <b>GetDeviceDetails</b>, and <b>Initialize</b>. These enumeration methods are no longer provided and standard Windows Audio APIs should be used for device enumeration instead.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>