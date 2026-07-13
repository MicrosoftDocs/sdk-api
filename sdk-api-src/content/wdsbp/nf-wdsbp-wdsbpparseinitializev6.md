---
UID: NF:wdsbp.WdsBpParseInitializev6
title: WdsBpParseInitializev6 function (wdsbp.h)
description: Receives a handle to the packet sent by the network boot program. (WdsBpParseInitializev6)
helpviewer_keywords: ["WDSBP_PK_TYPE_BCD","WDSBP_PK_TYPE_DHCP","WDSBP_PK_TYPE_DHCPV6","WDSBP_PK_TYPE_WDSNBP","WdsBpParseInitializev6","WdsBpParseInitializev6 function [Windows Deployment Services]","wds.wdsbpparseinitializev6","wdsbp/WdsBpParseInitializev6"]
old-location: wds\wdsbpparseinitializev6.htm
tech.root: wds
ms.assetid: 6387DA64-CE65-4C6B-9313-B062FA24D8C9
ms.date: 12/05/2018
ms.keywords: WDSBP_PK_TYPE_BCD, WDSBP_PK_TYPE_DHCP, WDSBP_PK_TYPE_DHCPV6, WDSBP_PK_TYPE_WDSNBP, WdsBpParseInitializev6, WdsBpParseInitializev6 function [Windows Deployment Services], wds.wdsbpparseinitializev6, wdsbp/WdsBpParseInitializev6
req.header: wdsbp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdsbp.lib
req.dll: Wdsbp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsBpParseInitializev6
 - wdsbp/WdsBpParseInitializev6
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsbp.dll
api_name:
 - WdsBpParseInitializev6
---

# WdsBpParseInitializev6 function


## -description

Receives a handle to the packet sent by the network boot program.

## -parameters

### -param pPacket [in]

A pointer to the packet received from the WDS client. The packet must be a valid DHCPv6 packet.

### -param uPacketLen [in]

The length of the packet, in bytes.

### -param pbPacketType [out, optional]

A value that indicates the type of boot program that sent the packet. The bit flags in the following table can be combined except <b>WDSBP_PK_TYPE_DHCP</b> and <b>WDSBP_PK_TYPE_DHCPV6</b> are mutually exclusive.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_DHCP"></a><a id="wdsbp_pk_type_dhcp"></a><dl>
<dt><b>WDSBP_PK_TYPE_DHCP</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The presence of this value indicates that the packet is a DHCP packet. This value is mutually exclusive of <b>WDSBP_PK_TYPE_DHCPV6</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_WDSNBP"></a><a id="wdsbp_pk_type_wdsnbp"></a><dl>
<dt><b>WDSBP_PK_TYPE_WDSNBP</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
This presence of this value indicates that the DHCPv6 packet came from the WDS network boot program. If this value is absent the type of client was not recognized.

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_BCD"></a><a id="wdsbp_pk_type_bcd"></a><dl>
<dt><b>WDSBP_PK_TYPE_BCD</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The presence of this value indicates that the packet contains a path to a Boot Configuration Data (BCD) file. 

</td>
</tr>
<tr>
<td width="40%"><a id="WDSBP_PK_TYPE_DHCPV6"></a><a id="wdsbp_pk_type_dhcpv6"></a><dl>
<dt><b>WDSBP_PK_TYPE_DHCPV6</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The presence of this value indicates that the packet is a DHCPV6 packet. This value is mutually exclusive of <b>WDSBP_PK_TYPE_DHCP</b>.

</td>
</tr>
</table>

### -param phHandle [out]

A handle to the packet. This handle can be used by the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpqueryoption">WdsBpQueryOption</a> function and must be closed using the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpclosehandle">WdsBpCloseHandle</a> function.

## -returns

If the function succeeds, the return is <b>S_OK</b>.
