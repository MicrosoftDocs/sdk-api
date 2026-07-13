---
UID: NF:segment.IMSVidStreamBufferSink3.get_LicenseErrorCode
title: IMSVidStreamBufferSink3::get_LicenseErrorCode (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IMSVidStreamBufferSink3 interface [Microsoft TV Technologies]","get_LicenseErrorCode method","IMSVidStreamBufferSink3.get_LicenseErrorCode","IMSVidStreamBufferSink3::get_LicenseErrorCode","IMSVidStreamBufferSink3get_LicenseErrorCode","get_LicenseErrorCode","get_LicenseErrorCode method [Microsoft TV Technologies]","get_LicenseErrorCode method [Microsoft TV Technologies]","IMSVidStreamBufferSink3 interface","mstv.imsvidstreambuffersink3_get_licenseerrorcode","segment/IMSVidStreamBufferSink3::get_LicenseErrorCode"]
old-location: mstv\imsvidstreambuffersink3_get_licenseerrorcode.htm
tech.root: mstv
ms.assetid: f20b8845-86ae-4fe9-9d2b-80341672843c
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSink3 interface [Microsoft TV Technologies],get_LicenseErrorCode method, IMSVidStreamBufferSink3.get_LicenseErrorCode, IMSVidStreamBufferSink3::get_LicenseErrorCode, IMSVidStreamBufferSink3get_LicenseErrorCode, get_LicenseErrorCode, get_LicenseErrorCode method [Microsoft TV Technologies], get_LicenseErrorCode method [Microsoft TV Technologies],IMSVidStreamBufferSink3 interface, mstv.imsvidstreambuffersink3_get_licenseerrorcode, segment/IMSVidStreamBufferSink3::get_LicenseErrorCode
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidStreamBufferSink3::get_LicenseErrorCode
 - segment/IMSVidStreamBufferSink3::get_LicenseErrorCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSink3.get_LicenseErrorCode
---

# IMSVidStreamBufferSink3::get_LicenseErrorCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_LicenseErrorCode</b> method returns the most recent error code relating to licenses.

## -parameters

### -param hres [out]

Receives an <b>HRESULT</b> value.

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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersink3">IMSVidStreamBufferSink3 Interface</a>