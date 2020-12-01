---
UID: NF:dhcpcsdk.DhcpRequestParams
title: DhcpRequestParams function (dhcpcsdk.h)
description: The DhcpRequestParams function enables callers to synchronously, or synchronously and persistently obtain DHCP data from a DHCP server.
helpviewer_keywords: ["DHCPCAPI_REQUEST_PERSISTENT","DHCPCAPI_REQUEST_SYNCHRONOUS","DhcpRequestParams","DhcpRequestParams function [DHCP]","_dhcp_dhcprequestparams","dhcp.dhcprequestparams","dhcpcsdk/DhcpRequestParams"]
old-location: dhcp\dhcprequestparams.htm
tech.root: DHCP
ms.assetid: 5fcbd1d9-8170-4c2b-ac98-6c04107c46e7
ms.date: 12/05/2018
ms.keywords: DHCPCAPI_REQUEST_PERSISTENT, DHCPCAPI_REQUEST_SYNCHRONOUS, DhcpRequestParams, DhcpRequestParams function [DHCP], _dhcp_dhcprequestparams, dhcp.dhcprequestparams, dhcpcsdk/DhcpRequestParams
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpRequestParams
 - dhcpcsdk/DhcpRequestParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - DhcpRequestParams
---

# DhcpRequestParams function


## -description

The 
<b>DhcpRequestParams</b> function enables callers to synchronously, or synchronously and persistently obtain DHCP data from a DHCP server.

## -parameters

### -param Flags [in]

Flags that specify the data being requested. This parameter is optional. The following possible values are supported and are not mutually exclusive:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DHCPCAPI_REQUEST_PERSISTENT"></a><a id="dhcpcapi_request_persistent"></a><dl>
<dt><b>DHCPCAPI_REQUEST_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
The request is persisted but no options are fetched.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCPCAPI_REQUEST_SYNCHRONOUS"></a><a id="dhcpcapi_request_synchronous"></a><dl>
<dt><b>DHCPCAPI_REQUEST_SYNCHRONOUS</b></dt>
</dl>
</td>
<td width="60%">
Options will be fetched from the server.

</td>
</tr>
</table>

### -param Reserved [in]

Reserved for future use. Must be set to <b>NULL</b>.

### -param AdapterName [in]

GUID of the adapter on which requested data is being made. Must be under 256 characters.

### -param ClassId [in]

Class identifier (ID) that should be used if DHCP INFORM messages are being transmitted onto the network. This parameter is optional.

### -param SendParams [in]

Optional data to be requested, in addition to the data requested in the <i>RecdParams</i> array. The <i>SendParams</i> parameter cannot contain any of the standard options that the DHCP client sends by default.

### -param RecdParams [in, out]

Array of DHCP data the caller is interested in receiving. This array must be empty prior to the 
<b>DhcpRequestParams</b> function call.

### -param Buffer [in]

Buffer used for storing the data associated with requests made in <i>RecdParams</i>.

### -param pSize [in, out]

Size of <i>Buffer</i>. 




Required size of the buffer, if it is insufficiently sized to hold the data, otherwise indicates size of the buffer which was successfully filled.

### -param RequestIdStr [in]

Application identifier (ID) used to facilitate a persistent request. Must be a printable string with no special characters (commas, backslashes, colons, or other illegal characters may not be used). The specified application identifier (ID) is used in a subsequent 
<b>DhcpUndoRequestParams</b> function call to clear the persistent request, as necessary.

## -returns

Returns ERROR_SUCCESS upon successful completion.

Upon return, <i>RecdParams</i> is filled with pointers to requested data, with corresponding data placed in <i>Buffer</i>. If <i>pSize</i> indicates that <i>Buffer</i> has insufficient space to store returned data, the 
<b>DhcpRequestParams</b> function returns ERROR_MORE_DATA, and returns the required buffer size in <i>pSize</i>. Note that the required size of <i>Buffer</i> may increase during the time that elapses between the initial function call's return and a subsequent call; therefore, the required size of <i>Buffer</i> (indicated in <i>pSize</i>) provides an indication of the approximate size required of <i>Buffer</i>, rather than guaranteeing that subsequent calls will return successfully if <i>Buffer</i> is set to the size indicated in <i>pSize</i>.

Other errors return appropriate Windows error codes.

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
Returned if the AdapterName parameter is over 256 characters long.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
Returned if the AdapterName parameter is over 256 characters long.

</td>
</tr>
</table>

## -remarks

DHCP clients store data obtained from a DHCP server in their local cache. If the DHCP client cache contains all data requested in the <i>RecdParams</i> array of a 
<b>DhcpRequestParams</b> function call, the client returns data from its cache. If requested data is not available in the client cache, the client processes the 
<b>DhcpRequestParams</b> function call by submitting a DHCP-INFORM message to the DHCP server.

When the client submits a DHCP-INFORM message to the DHCP server, it includes any requests provided in the optional <i>SendParams</i> parameter, and provides the Class identifier (ID) specified in the <i>ClassId</i> parameter, if provided.

Clients can also specify that DHCP data be retrieved from the DHCP server each time the DHCP client boots, which is considered a persistent request. To enable persistent requests, the caller must specify the <i>RequestIdStr</i> parameter, and also specify the additional <b>DHCPAPI_REQUEST_PERSISTENT</b> flag in the <i>dwFlags</i> parameter. This persistent request capability is especially useful when clients need to automatically request application-critical information at each boot. To disable a persist request, clients must call the 
 function.

<div class="alert"><b>Note</b>  The callers of this API must not make blocking calls to this API, since it can take up to a maximum of 2 minutes to return a code or status. UI behaviors in particular should not block on the return of this call, since it can introduce a significant delay in UI response time.</div>
<div> </div>
For more information about DHCP INFORM messages, and other standards-based information about DHCP, consult 
<a href="/previous-versions/windows/desktop/dhcp/about-dynamic-host-configuration-protocol">DHCP Standards</a>.

To see the 
<b>DhcpRequestParams</b> function in use, see 
<a href="/previous-versions/windows/desktop/dhcp/dhcp-client-api-examples">DHCP Examples</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/windows/win32/api/dhcpcsdk/ns-dhcpcsdk-dhcpcapi_params_array">DHCPCAPI_PARAMS_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapiinitialize">DhcpCApiInitialize</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpundorequestparams">DhcpUndoRequestParams</a>