---
UID: NF:rend.ITILSConfig.put_Port
title: ITILSConfig::put_Port (rend.h)
description: The put_Port method sets the port number used to connect to the server of a specified ILS directory.
helpviewer_keywords: ["ITILSConfig interface [TAPI 2.2]","put_Port method","ITILSConfig.put_Port","ITILSConfig::put_Port","_tapi3_itilsconfig_put_port","put_Port","put_Port method [TAPI 2.2]","put_Port method [TAPI 2.2]","ITILSConfig interface","rend/ITILSConfig::put_Port","tapi3.itilsconfig_put_port"]
old-location: tapi3\itilsconfig_put_port.htm
tech.root: tapi3
ms.assetid: 9d911a9c-6538-4919-9110-0425c53f91c4
ms.date: 12/05/2018
ms.keywords: ITILSConfig interface [TAPI 2.2],put_Port method, ITILSConfig.put_Port, ITILSConfig::put_Port, _tapi3_itilsconfig_put_port, put_Port, put_Port method [TAPI 2.2], put_Port method [TAPI 2.2],ITILSConfig interface, rend/ITILSConfig::put_Port, tapi3.itilsconfig_put_port
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
 - ITILSConfig::put_Port
 - rend/ITILSConfig::put_Port
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
 - ITILSConfig.put_Port
---

# ITILSConfig::put_Port


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>put_Port</b> method sets the port number used to connect to the server of a specified ILS directory.

## -parameters

### -param Port [in]

The port number that will be used to connect to the server. This can be any port number in the range of 16-bit unsigned integers.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>Port</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RND_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
A successful connection has been made. Port cannot be reset.

</td>
</tr>
</table>

## -remarks

Applications use this method only if they need to connect to custom-configured ILS servers listening on strange ports that are not listed in the Active Directory. By default, the Rendezvous control automatically tries to use ports 1002 and 389, the usual ILS ports, for connecting to application-specified ILS servers. Also, the Rendezvous control automatically uses whatever port is published in the Active Directory for ILS servers retrieved from there.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itilsconfig">ITILSConfig</a>



<a href="/windows/desktop/api/rend/nf-rend-itilsconfig-get_port">ITILSConfig::get_Port</a>