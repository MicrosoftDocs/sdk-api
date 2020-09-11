---
UID: NN:mbnapi.IMbnRadioEvents
title: IMbnRadioEvents (mbnapi.h)
description: Notification interface used to indicate a change in the radio state as well as the completion of a programatic change in the state .
helpviewer_keywords: ["IMbnRadioEvents","IMbnRadioEvents interface [Microsoft Broadband Networks]","IMbnRadioEvents interface [Microsoft Broadband Networks]","described","mbn.imbnradioevents","mbnapi/IMbnRadioEvents"]
old-location: mbn\imbnradioevents.htm
tech.root: mbn
ms.assetid: f02fa823-c1ca-4867-981d-cb3107f7291b
ms.date: 12/05/2018
ms.keywords: IMbnRadioEvents, IMbnRadioEvents interface [Microsoft Broadband Networks], IMbnRadioEvents interface [Microsoft Broadband Networks],described, mbn.imbnradioevents, mbnapi/IMbnRadioEvents
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnRadioEvents
 - mbnapi/IMbnRadioEvents
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnRadioEvents
---

# IMbnRadioEvents interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification interface used to indicate a change in the radio state as well as the completion of a programatic change in the state .

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRadioEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRadioEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnRadioEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnradioevents-onradiostatechange">OnRadioStateChange</a>
</td>
<td align="left" width="63%">
The radio state of the device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnradioevents-onsetsoftwareradiostatecomplete">OnSetSoftwareRadioStateComplete</a>
</td>
<td align="left" width="63%">
A set software radio state operation has completed.

</td>
</tr>
</table>

## -remarks

The following procedure describes how to register for notifications.

<ol>
<li>Get an <a href="https://msdn.microsoft.com/library/ms683857(VS.85).aspx">IConnectionPointContainer</a> interface by calling <b>QueryInterface</b> on an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanager">IMbnInterfaceManager</a> object.</li>
<li>Call <a href="https://msdn.microsoft.com/library/ms692476(VS.85).aspx">FindConnectionPoint</a> on the returned interface and pass <b>IID_IMbnRadioEvents</b> to <i>riid</i>.</li>
<li>Call <a href="https://msdn.microsoft.com/library/ms678815(VS.85).aspx">Advise</a> on the returned connection point and pass a pointer to an <b>IUnknown</b> interface on an object that implements <b>IMbnRadioEvents</b> to <i>pUnk</i>.</li>
</ol>
Notifications can be terminated by calling <a href="https://msdn.microsoft.com/library/ms686608(VS.85).aspx">Unadvise</a> on the connection point returned in step 2.

To view some code that registers for COM notifications, see the Client section of the <a href="https://docs.microsoft.com/en-us/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points">COM Connection Points</a> article.

