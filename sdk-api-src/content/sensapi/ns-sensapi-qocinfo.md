---
UID: NS:sensapi.tagQOCINFO
title: QOCINFO (sensapi.h)
description: The QOCINFO structure is returned by the IsDestinationReachable function and provides Quality of Connection information to the caller.
helpviewer_keywords: ["*LPQOCINFO","LPQOCINFO","LPQOCINFO structure pointer [SENS]","NETWORK_ALIVE_AOL","NETWORK_ALIVE_LAN","NETWORK_ALIVE_WAN","QOCINFO","QOCINFO structure [SENS]","_zaw_qocinfo","sens.qocinfo","sensapi/LPQOCINFO","sensapi/QOCINFO","syncmgr.qocinfo"]
old-location: sens\qocinfo.htm
tech.root: Sens
ms.assetid: 1f78a7c5-b3c7-4f21-8848-58cfb481f4bb
ms.date: 12/05/2018
ms.keywords: '*LPQOCINFO, LPQOCINFO, LPQOCINFO structure pointer [SENS], NETWORK_ALIVE_AOL, NETWORK_ALIVE_LAN, NETWORK_ALIVE_WAN, QOCINFO, QOCINFO structure [SENS], _zaw_qocinfo, sens.qocinfo, sensapi/LPQOCINFO, sensapi/QOCINFO, syncmgr.qocinfo'
req.header: sensapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: QOCINFO, *LPQOCINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQOCINFO
 - sensapi/tagQOCINFO
 - LPQOCINFO
 - sensapi/LPQOCINFO
 - QOCINFO
 - sensapi/QOCINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sensapi.h
api_name:
 - QOCINFO
---

# QOCINFO structure


## -description

The 
<b>QOCINFO</b> structure is returned by the 
<a href="/windows/desktop/api/sensapi/nf-sensapi-isdestinationreachablea">IsDestinationReachable</a> function and provides Quality of Connection information to the caller.

## -struct-fields

### -field dwSize

Upon calling 
<a href="/windows/desktop/api/sensapi/nf-sensapi-isdestinationreachablea">IsDestinationReachable</a>, the caller must specify the size of the <b>QOCINFO</b> structure being provided to the function using dwSize. The size should be specified in bytes. Upon return from <a href="/windows/desktop/api/sensapi/nf-sensapi-isdestinationreachablea">IsDestinationReachable</a>, dwSize contains the size of the provided structure in bytes.

### -field dwFlags

Provides information on the type of network connection available. The following table lists the possible values.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETWORK_ALIVE_LAN"></a><a id="network_alive_lan"></a><dl>
<dt><b>NETWORK_ALIVE_LAN</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The computer has one or more active LAN cards.

</td>
</tr>
<tr>
<td width="40%"><a id="NETWORK_ALIVE_WAN"></a><a id="network_alive_wan"></a><dl>
<dt><b>NETWORK_ALIVE_WAN</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The computer has one or more active RAS connections.

</td>
</tr>
<tr>
<td width="40%"><a id="NETWORK_ALIVE_AOL"></a><a id="network_alive_aol"></a><dl>
<dt><b>NETWORK_ALIVE_AOL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This flag is not supported.

</td>
</tr>
</table>

### -field dwInSpeed

Speed of data coming in from the destination in bytes per second.

### -field dwOutSpeed

Speed of data sent to the destination in bytes per second.

## -see-also

<a href="/windows/desktop/api/sensapi/nf-sensapi-isdestinationreachablea">IsDestinationReachable</a>