---
UID: NF:mfidl.IMFContentEnabler.GetEnableURL
title: IMFContentEnabler::GetEnableURL (mfidl.h)
description: Retrieves a URL for performing a manual content enabling action.
helpviewer_keywords: ["1a44216d-36e5-4b5c-9585-5297d5e429f9","GetEnableURL","GetEnableURL method [Media Foundation]","GetEnableURL method [Media Foundation]","IMFContentEnabler interface","IMFContentEnabler interface [Media Foundation]","GetEnableURL method","IMFContentEnabler.GetEnableURL","IMFContentEnabler::GetEnableURL","mf.imfcontentenabler_getenableurl","mfidl/IMFContentEnabler::GetEnableURL"]
old-location: mf\imfcontentenabler_getenableurl.htm
tech.root: mf
ms.assetid: 1a44216d-36e5-4b5c-9585-5297d5e429f9
ms.date: 12/05/2018
ms.keywords: 1a44216d-36e5-4b5c-9585-5297d5e429f9, GetEnableURL, GetEnableURL method [Media Foundation], GetEnableURL method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],GetEnableURL method, IMFContentEnabler.GetEnableURL, IMFContentEnabler::GetEnableURL, mf.imfcontentenabler_getenableurl, mfidl/IMFContentEnabler::GetEnableURL
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
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFContentEnabler::GetEnableURL
 - mfidl/IMFContentEnabler::GetEnableURL
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
 - IMFContentEnabler.GetEnableURL
---

# IMFContentEnabler::GetEnableURL


## -description

Retrieves a URL for performing a manual content enabling action.

## -parameters

### -param ppwszURL [out]

Receives a pointer to a buffer that contains the URL. The caller must release the memory for the buffer by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcchURL [out]

Receives the number of characters returned in <i>ppwszURL</i>, including the terminating NULL character.

### -param pTrustStatus [in, out]

Receives a member of the <a href="/windows/win32/api/mfidl/ne-mfidl-mf_url_trust_status">MF_URL_TRUST_STATUS</a> enumeration indicating whether the URL is trusted.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No URL is available.

</td>
</tr>
</table>

## -remarks

If the enabling action can be performed by navigating to a URL, this method returns the URL. If no such URL exists, the method returns a failure code.

The purpose of the URL depends on the content enabler type, which is obtained by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabletype">IMFContentEnabler::GetEnableType</a>.

<table>
<tr>
<th>Enable type</th>
<th>Purpose of URL</th>
</tr>
<tr>
<td>Individualization</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>License acquisition</td>
<td>URL to obtain the license. Call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata">IMFContentEnabler::GetEnableData</a> and submit the data to the URL as an HTTP POST request. To receive notification when the license is acquired, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable">IMFContentEnabler::MonitorEnable</a>.</td>
</tr>
<tr>
<td>Revocation</td>
<td>URL to a webpage where the user can download and install an updated component.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a>