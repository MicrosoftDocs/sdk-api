---
UID: NF:winnetwk.MultinetGetConnectionPerformanceW
title: MultinetGetConnectionPerformanceW function (winnetwk.h)
description: Returns information about the expected performance of a connection used to access a network resource. (Unicode)
helpviewer_keywords: ["MultinetGetConnectionPerformance", "MultinetGetConnectionPerformance function [Windows Networking (WNet)]", "MultinetGetConnectionPerformanceW", "_win32_multinetgetconnectionperformance", "lpLocalName", "lpProvider", "lpRemoteName", "winnetwk/MultinetGetConnectionPerformance", "winnetwk/MultinetGetConnectionPerformanceW", "wnet.multinetgetconnectionperformance"]
old-location: wnet\multinetgetconnectionperformance.htm
tech.root: WNet
ms.assetid: 3ec4a397-e0d4-419c-9e12-6d76a87b1ca0
ms.date: 12/05/2018
ms.keywords: MultinetGetConnectionPerformance, MultinetGetConnectionPerformance function [Windows Networking (WNet)], MultinetGetConnectionPerformanceA, MultinetGetConnectionPerformanceW, _win32_multinetgetconnectionperformance, lpLocalName, lpProvider, lpRemoteName, winnetwk/MultinetGetConnectionPerformance, winnetwk/MultinetGetConnectionPerformanceA, winnetwk/MultinetGetConnectionPerformanceW, wnet.multinetgetconnectionperformance
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MultinetGetConnectionPerformanceW (Unicode) and MultinetGetConnectionPerformanceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MultinetGetConnectionPerformanceW
 - winnetwk/MultinetGetConnectionPerformanceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - MultinetGetConnectionPerformance
 - MultinetGetConnectionPerformanceA
 - MultinetGetConnectionPerformanceW
---

# MultinetGetConnectionPerformanceW function


## -description

The
				<b>MultinetGetConnectionPerformance</b> function returns information about the expected performance of a connection used to access a network resource.

## -parameters

### -param lpNetResource [in]

A pointer to a 
<a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure that specifies the network resource. The following members have specific meanings in this context.

<table>
<tr>
<th>Member</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="lpLocalName"></a><a id="lplocalname"></a><a id="LPLOCALNAME"></a><dl>
<dt><b><b>lpLocalName</b></b></dt>
</dl>
</td>
<td width="60%">
A pointer to a buffer that specifies a local device, such as "F:" or "LPT1", that is redirected to a network resource to be queried. 




If this member is <b>NULL</b> or an empty string, the network resource is specified in the <i>lpRemoteName</i> member. If this flag specifies a local device, <i>lpRemoteName</i> is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="lpRemoteName"></a><a id="lpremotename"></a><a id="LPREMOTENAME"></a><dl>
<dt><b><b>lpRemoteName</b></b></dt>
</dl>
</td>
<td width="60%">
A pointer to a network resource to query. The resource must currently have an established connection. For example, if the resource is a file on a file server, then having the file open will ensure the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="lpProvider"></a><a id="lpprovider"></a><a id="LPPROVIDER"></a><dl>
<dt><b><b>lpProvider</b></b></dt>
</dl>
</td>
<td width="60%">
Usually set to <b>NULL</b>, but can be a pointer to the owner (provider) of the resource if the network on which the resource resides is known. 




If the <i>lpProvider</i> member is not <b>NULL</b>, the system attempts to return information only about the named network.

</td>
</tr>
</table>

### -param lpNetConnectInfoStruct [out]

A pointer to the 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netconnectinfostruct">NETCONNECTINFOSTRUCT</a> structure that receives the data.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is a 
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The network resource does not supply this information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpLocalName</b> member of the <a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure pointed to by the  <i>lpNetResource</i> parameter does not specify a redirected device, or the <i>lpRemoteName</i> member does not specify the name of a resource that is currently connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NET_OR_BAD_PATH</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed, either because a network component is not started, or because the specified resource name is not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The local device specified by the <i>lpLocalName</i> member is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NET_NAME</b></dt>
</dl>
</td>
<td width="60%">
The network name cannot be found. This error is returned if the <b>lpLocalName</b> member of the <a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure pointed to by the  <i>lpNetResource</i> parameter was <b>NULL</b> and the <b>lpRemoteName</b> member of the <b>NETRESOURCE</b> structure pointed to by the  <i>lpNetResource</i> was also or <b>NULL</b> or could not recognized by any network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
An attempt to access an invalid address. This error is returned if the <i>lpNetResource</i> or <i>lpNetConnectInfoStruct</i> parameters were <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A bad parameter was passed. This error is returned if the <i>lpNetConnectInfoStruct</i> parameter does not point to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netconnectinfostruct">NETCONNECTINFOSTRUCT</a> structure in which the <b>cbStructure</b> member is filled with the proper structure size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. To obtain a description of the error, call 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a>.

</td>
</tr>
</table>

## -remarks

The <b>MultinetGetConnectionPerformance</b> function returns the information in a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netconnectinfostruct">NETCONNECTINFOSTRUCT</a> structure.

The information returned by the 
<b>MultinetGetConnectionPerformance</b> function is an estimate only. Network traffic and routing can affect the accuracy of the results returned.

Note that the 
<b>MultinetGetConnectionPerformance</b> function can be used only to request information for a local device that is redirected to a network resource, or for a network resource to which there is currently a connection.

If a UNC path is specified in the <b>lpRemoteName</b> member of the <a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a> structure pointed to by the <i>lpNetResource</i> parameter,  the <b>lpRemoteName</b> member must be a directory name, not  a filename. 

A typical way to use this function would be to open a file on a network server (which would ensure that there is a connection to the file), call this function, and use the results to make decisions about how to manage file I/O. For example, you can decide whether to read the entire file into a temporary file on the client or directly access the file on the server.





> [!NOTE]
> The winnetwk.h header defines MultinetGetConnectionPerformance as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netconnectinfostruct">NETCONNECTINFOSTRUCT</a>



<a href="ns-winnetwk-netresourcew.md">NETRESOURCE</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
