---
UID: NF:mfidl.IMFHttpDownloadRequest.GetTotalLength
title: IMFHttpDownloadRequest::GetTotalLength (mfidl.h)
description: Invoked by Microsoft Media Foundation to retrieve the total length of the resource that is being downloaded, if known.
helpviewer_keywords: ["GetTotalLength","GetTotalLength method [Media Foundation]","GetTotalLength method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","GetTotalLength method","IMFHttpDownloadRequest.GetTotalLength","IMFHttpDownloadRequest::GetTotalLength","mf.imfhttpdownloadrequest_gettotallength","mfidl/IMFHttpDownloadRequest::GetTotalLength"]
old-location: mf\imfhttpdownloadrequest_gettotallength.htm
tech.root: mf
ms.assetid: E52D44B5-F24F-4234-A67D-0F764A3864DB
ms.date: 12/05/2018
ms.keywords: GetTotalLength, GetTotalLength method [Media Foundation], GetTotalLength method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],GetTotalLength method, IMFHttpDownloadRequest.GetTotalLength, IMFHttpDownloadRequest::GetTotalLength, mf.imfhttpdownloadrequest_gettotallength, mfidl/IMFHttpDownloadRequest::GetTotalLength
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFHttpDownloadRequest::GetTotalLength
 - mfidl/IMFHttpDownloadRequest::GetTotalLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFHttpDownloadRequest.GetTotalLength
---

# IMFHttpDownloadRequest::GetTotalLength


## -description

Invoked by Microsoft Media Foundation to retrieve the total length of the resource that is being downloaded, if known.

## -parameters

### -param pqwTotalLength [out]

The total length, in bytes, of the resource being downloaded, if known. If not known, set to <b>MAX_ULONG</b> (0xFFFFFFFFFFFFFFFF).

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
Successfully completed the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pqwTotalLength</i> parameter is an invalid pointer.

</td>
</tr>
</table>

## -remarks

Microsoft Media Foundation invokes <b>GetTotalLength</b> only after having successfully invoked <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a>. The total length of the resource may be larger than the amount of data returned by the server in the current response. For example, if the request included the HTTP “Range” header, the data returned in the response may be less than total length of the resource. The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-getrangeendoffset">GetRangeEndOffset</a> method can be used to calculate how much data is returned in the current response.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>