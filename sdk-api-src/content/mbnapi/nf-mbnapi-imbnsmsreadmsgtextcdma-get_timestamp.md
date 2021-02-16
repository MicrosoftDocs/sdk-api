---
UID: NF:mbnapi.IMbnSmsReadMsgTextCdma.get_Timestamp
title: IMbnSmsReadMsgTextCdma::get_Timestamp (mbnapi.h)
description: The timestamp of a message.
helpviewer_keywords: ["IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks]","Timestamp property","IMbnSmsReadMsgTextCdma.Timestamp","IMbnSmsReadMsgTextCdma.get_Timestamp","IMbnSmsReadMsgTextCdma::Timestamp","IMbnSmsReadMsgTextCdma::get_Timestamp","Timestamp property [Microsoft Broadband Networks]","Timestamp property [Microsoft Broadband Networks]","IMbnSmsReadMsgTextCdma interface","get_Timestamp","mbn.imbnsmsreadmsgtextcdma_timestamp","mbnapi/IMbnSmsReadMsgTextCdma::Timestamp","mbnapi/IMbnSmsReadMsgTextCdma::get_Timestamp"]
old-location: mbn\imbnsmsreadmsgtextcdma_timestamp.htm
tech.root: mbn
ms.assetid: 178de8ed-b7ab-4a1a-a533-8dcffbdb8499
ms.date: 12/05/2018
ms.keywords: IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks],Timestamp property, IMbnSmsReadMsgTextCdma.Timestamp, IMbnSmsReadMsgTextCdma.get_Timestamp, IMbnSmsReadMsgTextCdma::Timestamp, IMbnSmsReadMsgTextCdma::get_Timestamp, Timestamp property [Microsoft Broadband Networks], Timestamp property [Microsoft Broadband Networks],IMbnSmsReadMsgTextCdma interface, get_Timestamp, mbn.imbnsmsreadmsgtextcdma_timestamp, mbnapi/IMbnSmsReadMsgTextCdma::Timestamp, mbnapi/IMbnSmsReadMsgTextCdma::get_Timestamp
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
 - IMbnSmsReadMsgTextCdma::get_Timestamp
 - mbnapi/IMbnSmsReadMsgTextCdma::get_Timestamp
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
 - IMbnSmsReadMsgTextCdma.Timestamp
 - IMbnSmsReadMsgTextCdma.get_Timestamp
---

# IMbnSmsReadMsgTextCdma::get_Timestamp


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The timestamp of a message.

This property is read-only.

## -parameters

## -remarks

The format of the timestamp string is "YY/MM/DD,HH:mm:SS±ZZ".

The following table defines the format of the timestamp string.


<table>
<tr>
<th>Field</th>
<th>Meaning</th>
<th>Example</th>
<th>Range</th>
</tr>
<tr>
<td>YY</td>
<td>Last 2 digits of the year</td>
<td>07 for 2007</td>
<td>00 through 99</td>
</tr>
<tr>
<td>MM</td>
<td>Month in double digits</td>
<td>01 for January</td>
<td>01 through 12</td>
</tr>
<tr>
<td>DD</td>
<td>Date in double digits</td>
<td>01 for the 1st</td>
<td>01 through 31</td>
</tr>
<tr>
<td>HH</td>
<td>Hours in 24 hour format</td>
<td>13 for 1PM</td>
<td>00 through 23</td>
</tr>
<tr>
<td>mm</td>
<td>Minutes in double digits</td>
<td>1 for 1 minute</td>
<td>00 through 59</td>
</tr>
<tr>
<td>SS</td>
<td>Seconds in double digits</td>
<td>01 for 1 second</td>
<td>00 though 59</td>
</tr>
<tr>
<td>ZZ</td>
<td>Time in relation to GMT</td>
<td>+01 for 1 hour greater</td>
<td>-12 through +13</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgtextcdma">IMbnSmsReadMsgTextCdma</a>