---
UID: NF:mbnapi.IMbnRadioEvents.OnSetSoftwareRadioStateComplete
title: IMbnRadioEvents::OnSetSoftwareRadioStateComplete (mbnapi.h)
description: Notification that a set software radio state operation has completed.
helpviewer_keywords: ["IMbnRadioEvents interface [Microsoft Broadband Networks]","OnSetSoftwareRadioStateComplete method","IMbnRadioEvents.OnSetSoftwareRadioStateComplete","IMbnRadioEvents::OnSetSoftwareRadioStateComplete","OnSetSoftwareRadioStateComplete","OnSetSoftwareRadioStateComplete method [Microsoft Broadband Networks]","OnSetSoftwareRadioStateComplete method [Microsoft Broadband Networks]","IMbnRadioEvents interface","S_OK","mbn.imbnradioevents_onsetsoftwareradiostatecomplete","mbnapi/IMbnRadioEvents::OnSetSoftwareRadioStateComplete"]
old-location: mbn\imbnradioevents_onsetsoftwareradiostatecomplete.htm
tech.root: mbn
ms.assetid: 0e62ff68-0a6b-4e22-9cce-0df5da14fa6a
ms.date: 12/05/2018
ms.keywords: IMbnRadioEvents interface [Microsoft Broadband Networks],OnSetSoftwareRadioStateComplete method, IMbnRadioEvents.OnSetSoftwareRadioStateComplete, IMbnRadioEvents::OnSetSoftwareRadioStateComplete, OnSetSoftwareRadioStateComplete, OnSetSoftwareRadioStateComplete method [Microsoft Broadband Networks], OnSetSoftwareRadioStateComplete method [Microsoft Broadband Networks],IMbnRadioEvents interface, S_OK, mbn.imbnradioevents_onsetsoftwareradiostatecomplete, mbnapi/IMbnRadioEvents::OnSetSoftwareRadioStateComplete
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
 - IMbnRadioEvents::OnSetSoftwareRadioStateComplete
 - mbnapi/IMbnRadioEvents::OnSetSoftwareRadioStateComplete
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
 - IMbnRadioEvents.OnSetSoftwareRadioStateComplete
---

# IMbnRadioEvents::OnSetSoftwareRadioStateComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification that a set software radio state operation has completed.

## -parameters

### -param newInterface [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnradio">IMbnRadio</a> interface representing the device for which a set radio state operation has completed.

### -param requestID [in]

The request ID set by the Mobile Broadband service to identify the request.

### -param status [in]

A status code that indicates the outcome of the set radio state operation.

A calling application can expect one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
</table>

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnradioevents">IMbnRadioEvents</a>