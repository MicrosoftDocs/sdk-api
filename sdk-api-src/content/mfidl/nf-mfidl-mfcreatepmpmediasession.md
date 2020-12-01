---
UID: NF:mfidl.MFCreatePMPMediaSession
title: MFCreatePMPMediaSession function (mfidl.h)
description: Creates an instance of the Media Session inside a Protected Media Path (PMP) process.
helpviewer_keywords: ["MFCreatePMPMediaSession","MFCreatePMPMediaSession function [Media Foundation]","cb492e68-3d8a-49b2-8c0b-bee8065b53a8","mf.mfcreatepmpmediasession","mfidl/MFCreatePMPMediaSession"]
old-location: mf\mfcreatepmpmediasession.htm
tech.root: mf
ms.assetid: cb492e68-3d8a-49b2-8c0b-bee8065b53a8
ms.date: 12/05/2018
ms.keywords: MFCreatePMPMediaSession, MFCreatePMPMediaSession function [Media Foundation], cb492e68-3d8a-49b2-8c0b-bee8065b53a8, mf.mfcreatepmpmediasession, mfidl/MFCreatePMPMediaSession
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreatePMPMediaSession
 - mfidl/MFCreatePMPMediaSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreatePMPMediaSession
---

# MFCreatePMPMediaSession function


## -description

Creates an instance of the <a href="/windows/desktop/medfound/media-session">Media Session</a> inside a Protected Media Path (PMP) process.

## -parameters

### -param dwCreationFlags

A member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfpmpsession_creation_flags">MFPMPSESSION_CREATION_FLAGS</a> enumeration that specifies how to create the session object.

### -param pConfiguration

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. This parameter can be <b>NULL</b>. See Remarks.

### -param ppMediaSession

Receives a pointer to the PMP Media Session's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a> interface. The caller must release the interface. Before releasing the last reference to the <b>IMFMediaSession</b> pointer, the application must call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown">IMFMediaSession::Shutdown</a> method.

### -param ppEnablerActivate

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface or the value <b>NULL</b>. If non-<b>NULL</b>, the caller must release the interface. See Remarks.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The function succeeded.

</td>
</tr>
</table>

## -remarks

You can use the <i>pConfiguration</i> parameter to set any of the following attributes:

<ul>
<li>
<a href="/windows/desktop/medfound/mf-session-content-protection-manager-attribute">MF_SESSION_CONTENT_PROTECTION_MANAGER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-global-time-attribute">MF_SESSION_GLOBAL_TIME</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-quality-manager-attribute">MF_SESSION_QUALITY_MANAGER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-remote-source-mode-attribute">MF_SESSION_REMOTE_SOURCE_MODE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-server-context-attribute">MF_SESSION_SERVER_CONTEXT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-topoloader-attribute">MF_SESSION_TOPOLOADER</a>
</li>
</ul>
If this function cannot create the PMP Media Session because a trusted binary was revoked, the <i>ppEnablerActivate</i> parameter receives an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface pointer. The application can use this pointer to create a content enabler object, which can then be used to download an updated binary:

<ol>
<li>Call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> with the interface identifier IID_IMFContentEnabler to get an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a> interface pointer.
          </li>
<li>Use that interface to download the updated binary.
          </li>
<li>Call <b>MFCreatePMPMediaSession</b> again.
          </li>
</ol>
If the function successfully creates the PMP Media Session, the <i>ppEnablerActivate</i> parameter receives the value <b>NULL</b>.

Do not make calls to the PMP Media Session from a thread that is processing a window message sent from another thread. To test whether the current thread falls into this category, call <a href="/windows/desktop/api/winuser/nf-winuser-insendmessage">InSendMessage</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession">MFCreateMediaSession</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>