---
UID: NN:mfidl.IMFRemoteDesktopPlugin
title: IMFRemoteDesktopPlugin (mfidl.h)
description: Modifies a topology for use in a Terminal Services environment.
helpviewer_keywords: ["75bb9bf8-12a7-430f-9943-18623aff9903","IMFRemoteDesktopPlugin","IMFRemoteDesktopPlugin interface [Media Foundation]","IMFRemoteDesktopPlugin interface [Media Foundation]","described","mf.imfremotedesktopplugin","mfidl/IMFRemoteDesktopPlugin"]
old-location: mf\imfremotedesktopplugin.htm
tech.root: mf
ms.assetid: 75bb9bf8-12a7-430f-9943-18623aff9903
ms.date: 12/05/2018
ms.keywords: 75bb9bf8-12a7-430f-9943-18623aff9903, IMFRemoteDesktopPlugin, IMFRemoteDesktopPlugin interface [Media Foundation], IMFRemoteDesktopPlugin interface [Media Foundation],described, mf.imfremotedesktopplugin, mfidl/IMFRemoteDesktopPlugin
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
 - IMFRemoteDesktopPlugin
 - mfidl/IMFRemoteDesktopPlugin
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
 - IMFRemoteDesktopPlugin
---

# IMFRemoteDesktopPlugin interface


## -description

Modifies a topology for use in a Terminal Services environment.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRemoteDesktopPlugin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFRemoteDesktopPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRemoteDesktopPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfremotedesktopplugin-updatetopology">UpdateTopology</a>
</td>
<td align="left" width="63%">
Modifies a topology for use in a Terminal Services environment.

</td>
</tr>
</table>

## -remarks

To use this interface, do the following:

<ol>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with the <b>SM_REMOTESESSION</b> flag. The function returns <b>TRUE</b> if the calling process is associated with a Terminal Services client session.
          </li>
<li>If <b>GetSystemMetrics</b> returns <b>TRUE</b>, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreateremotedesktopplugin">MFCreateRemoteDesktopPlugin</a>. This function returns a pointer to the <b>IMFRemoteDesktopPlugin</b> interface.
          </li>
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfremotedesktopplugin-updatetopology">UpdateTopology</a> with a pointer to the topology.
          </li>
</ol>
The application must call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfremotedesktopplugin-updatetopology">UpdateTopology</a> before calling <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a> on the Media Session.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

