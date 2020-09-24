---
UID: NF:netioapi.GetTeredoPort
title: GetTeredoPort function (netioapi.h)
description: Retrieves the dynamic UDP port number used by the Teredo client on the local computer.
helpviewer_keywords: ["GetTeredoPort","GetTeredoPort function [IP Helper]","iphlp.getteredoport","netioapi/GetTeredoPort"]
old-location: iphlp\getteredoport.htm
tech.root: IpHlp
ms.assetid: 59d3764d-e560-4474-a73e-ab50bbddbf07
ms.date: 12/05/2018
ms.keywords: GetTeredoPort, GetTeredoPort function [IP Helper], iphlp.getteredoport, netioapi/GetTeredoPort
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTeredoPort
 - netioapi/GetTeredoPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetTeredoPort
---

# GetTeredoPort function


## -description

The 
<b>GetTeredoPort</b> function  retrieves the dynamic UDP port number used by the Teredo client on the local computer.

## -parameters

### -param Port [out]

A pointer to the  UDP port number. On successful return, this parameter will be filled with the port number used by the Teredo client.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Port</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The device is not ready. This error is returned if the Teredo client is not started on the local computer. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv6 stack is on the local computer. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetTeredoPort</b> function is defined on Windows Vista and later. 

The <b>GetTeredoPort</b> function retrieves the current UDP port number used by the Teredo client for the Teredo service port. The Teredo port is dynamic and can change any time the Teredo client is restarted on the local computer. An application can  register to be notified when the Teredo service port changes by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange">NotifyTeredoPortChange</a> function. 

The Teredo client also uses static UDP port 3544 for listening to multicast traffic sent on multicast IPv4 address 224.0.0.253 as defined in RFC 4380. For more information, see <a href="https://www.ietf.org/rfc/rfc4380.txt">http://www.ietf.org/rfc/rfc4380.txt</a>.

The <b>GetTeredoPort</b> function is used primarily by firewall applications in order to configure the appropriate exceptions to allow incoming and outgoing Teredo traffic.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable">NotifyStableUnicastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange">NotifyTeredoPortChange</a>