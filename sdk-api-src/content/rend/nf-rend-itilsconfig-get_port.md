---
UID: NF:rend.ITILSConfig.get_Port
title: ITILSConfig::get_Port (rend.h)
description: The get_Port method gets the port number used to connect to the server of a given ILS directory.
helpviewer_keywords: ["ITILSConfig interface [TAPI 2.2]","get_Port method","ITILSConfig.get_Port","ITILSConfig::get_Port","_tapi3_itilsconfig_get_port","get_Port","get_Port method [TAPI 2.2]","get_Port method [TAPI 2.2]","ITILSConfig interface","rend/ITILSConfig::get_Port","tapi3.itilsconfig_get_port"]
old-location: tapi3\itilsconfig_get_port.htm
tech.root: tapi3
ms.assetid: 7aa0a8e7-6799-4685-92a0-c2ce610d0e06
ms.date: 12/05/2018
ms.keywords: ITILSConfig interface [TAPI 2.2],get_Port method, ITILSConfig.get_Port, ITILSConfig::get_Port, _tapi3_itilsconfig_get_port, get_Port, get_Port method [TAPI 2.2], get_Port method [TAPI 2.2],ITILSConfig interface, rend/ITILSConfig::get_Port, tapi3.itilsconfig_get_port
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITILSConfig::get_Port
 - rend/ITILSConfig::get_Port
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITILSConfig.get_Port
---

# ITILSConfig::get_Port


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Port</b> method gets the port number used to connect to the server of a given ILS directory.

## -parameters

### -param pPort [out]

Pointer to receive the port number used in the connection.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itilsconfig">ITILSConfig</a>



<a href="/windows/desktop/api/rend/nf-rend-itilsconfig-put_port">ITILSConfig::put_Port</a>