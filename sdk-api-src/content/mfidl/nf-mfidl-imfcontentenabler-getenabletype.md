---
UID: NF:mfidl.IMFContentEnabler.GetEnableType
title: IMFContentEnabler::GetEnableType (mfidl.h)
description: Retrieves the type of operation that this content enabler performs.
helpviewer_keywords: ["9fe597d8-788c-48c4-a21a-0b91a890710f","GetEnableType","GetEnableType method [Media Foundation]","GetEnableType method [Media Foundation]","IMFContentEnabler interface","IMFContentEnabler interface [Media Foundation]","GetEnableType method","IMFContentEnabler.GetEnableType","IMFContentEnabler::GetEnableType","mf.imfcontentenabler_getenabletype","mfidl/IMFContentEnabler::GetEnableType"]
old-location: mf\imfcontentenabler_getenabletype.htm
tech.root: mf
ms.assetid: 9fe597d8-788c-48c4-a21a-0b91a890710f
ms.date: 12/05/2018
ms.keywords: 9fe597d8-788c-48c4-a21a-0b91a890710f, GetEnableType, GetEnableType method [Media Foundation], GetEnableType method [Media Foundation],IMFContentEnabler interface, IMFContentEnabler interface [Media Foundation],GetEnableType method, IMFContentEnabler.GetEnableType, IMFContentEnabler::GetEnableType, mf.imfcontentenabler_getenabletype, mfidl/IMFContentEnabler::GetEnableType
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
 - IMFContentEnabler::GetEnableType
 - mfidl/IMFContentEnabler::GetEnableType
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
 - IMFContentEnabler.GetEnableType
---

# IMFContentEnabler::GetEnableType


## -description

Retrieves the type of operation that this content enabler performs.

## -parameters

### -param pType [out]

Receives a GUID that identifies the type of operation. An application can tailor its user interface (UI) strings for known operation types. See Remarks.

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
</table>

## -remarks

The following GUIDs are defined for the <i>pType</i> parameter.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>MFENABLETYPE_MF_RebootRequired</td>
<td>The user must reboot his or her computer.</td>
</tr>
<tr>
<td>MFENABLETYPE_MF_UpdateRevocationInformation</td>
<td>Update revocation information.</td>
</tr>
<tr>
<td>MFENABLETYPE_MF_UpdateUntrustedComponent</td>
<td>Update untrusted components.</td>
</tr>
<tr>
<td>MFENABLETYPE_WMDRMV1_LicenseAcquisition</td>
<td>License acquisition for Windows Media Digital Rights Management (DRM) version 1.</td>
</tr>
<tr>
<td>MFENABLETYPE_WMDRMV7_Individualization</td>
<td>Individualization.</td>
</tr>
<tr>
<td>MFENABLETYPE_WMDRMV7_LicenseAcquisition</td>
<td>License acquisition for Windows Media DRM version 7 or later.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a>