---
UID: NF:mfidl.MFCreateMediaSession
title: MFCreateMediaSession function (mfidl.h)
description: Creates the Media Session in the application's process.
helpviewer_keywords: ["86b2b5ec-231c-4943-9add-1a5a60e72268","MFCreateMediaSession","MFCreateMediaSession function [Media Foundation]","mf.mfcreatemediasession","mfidl/MFCreateMediaSession"]
old-location: mf\mfcreatemediasession.htm
tech.root: mf
ms.assetid: 86b2b5ec-231c-4943-9add-1a5a60e72268
ms.date: 12/05/2018
ms.keywords: 86b2b5ec-231c-4943-9add-1a5a60e72268, MFCreateMediaSession, MFCreateMediaSession function [Media Foundation], mf.mfcreatemediasession, mfidl/MFCreateMediaSession
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMediaSession
 - mfidl/MFCreateMediaSession
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
 - MFCreateMediaSession
---

# MFCreateMediaSession function


## -description

Creates the <a href="/windows/desktop/medfound/media-session">Media Session</a> in the application's process.

## -parameters

### -param pConfiguration

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. This parameter can be <b>NULL</b>. See Remarks.

### -param ppMediaSession

Receives a pointer to the Media Session's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a> interface. The caller must release the interface. Before releasing the last reference to the <b>IMFMediaSession</b> pointer, the application must call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown">IMFMediaSession::Shutdown</a> method.

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

If your application does not play protected content, you can use this function to create the Media Session in the application's process. To use the Media Session for protected content, you must call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a>.
      

You can use the <i>pConfiguration</i> parameter to specify any of the following attributes:
      
        

<ul>
<li>
<a href="/windows/desktop/medfound/mf-session-global-time-attribute">MF_SESSION_GLOBAL_TIME</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-quality-manager-attribute">MF_SESSION_QUALITY_MANAGER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-session-topoloader-attribute">MF_SESSION_TOPOLOADER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-low-latency">MF_LOW_LATENCY</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/about-the-media-session">About the Media Session</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-session">Media Session</a>