---
UID: NF:mbnapi.IMbnSmsReadMsgPdu.get_PduData
title: IMbnSmsReadMsgPdu::get_PduData (mbnapi.h)
description: The PDU message in hexadecimal format as used by GSM devices.
helpviewer_keywords: ["IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks]","PduData property","IMbnSmsReadMsgPdu.PduData","IMbnSmsReadMsgPdu.get_PduData","IMbnSmsReadMsgPdu::PduData","IMbnSmsReadMsgPdu::get_PduData","PduData property [Microsoft Broadband Networks]","PduData property [Microsoft Broadband Networks]","IMbnSmsReadMsgPdu interface","get_PduData","mbn.imbnsmsreadmsgpdu_pdudata","mbnapi/IMbnSmsReadMsgPdu::PduData","mbnapi/IMbnSmsReadMsgPdu::get_PduData"]
old-location: mbn\imbnsmsreadmsgpdu_pdudata.htm
tech.root: mbn
ms.assetid: 709dd6dd-c54d-4a46-bc29-f68229feb97d
ms.date: 12/05/2018
ms.keywords: IMbnSmsReadMsgPdu interface [Microsoft Broadband Networks],PduData property, IMbnSmsReadMsgPdu.PduData, IMbnSmsReadMsgPdu.get_PduData, IMbnSmsReadMsgPdu::PduData, IMbnSmsReadMsgPdu::get_PduData, PduData property [Microsoft Broadband Networks], PduData property [Microsoft Broadband Networks],IMbnSmsReadMsgPdu interface, get_PduData, mbn.imbnsmsreadmsgpdu_pdudata, mbnapi/IMbnSmsReadMsgPdu::PduData, mbnapi/IMbnSmsReadMsgPdu::get_PduData
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
 - IMbnSmsReadMsgPdu::get_PduData
 - mbnapi/IMbnSmsReadMsgPdu::get_PduData
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
 - IMbnSmsReadMsgPdu.PduData
 - IMbnSmsReadMsgPdu.get_PduData
---

# IMbnSmsReadMsgPdu::get_PduData


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The PDU message in hexadecimal format as used by GSM devices.

This property is read-only.

## -parameters

## -remarks

  For GSM devices, this data in <i>PduData</i> is compliant to the PDU structure defined in 3GPP TS 27.005 and 3GPP TS 23.040.

The table below shows an example of how a PDU message containing the message "Hello" would be structured.


<table>
<tr>
<th>Example</th>
<td>07</td>
<td>91198994000010</td>
<td>11000A9189945086180000AA05C8329BFD06</td>
</tr>
<tr>
<th>Contents</th>
<td>Size of Service Center Address</td>
<td>Service Center Address</td>
<td>PDU in hexadecimal format</td>
</tr>
<tr>
<th>Size</th>
<td>1 byte</td>
<td>Variable</td>
<td>Variable</td>
</tr>
</table>
 



For CDMA devices, this property returns <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgpdu">IMbnSmsReadMsgPdu</a>