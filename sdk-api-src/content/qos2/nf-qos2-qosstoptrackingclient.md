---
UID: NF:qos2.QOSStopTrackingClient
title: QOSStopTrackingClient function (qos2.h)
description: The QOSStopTrackingClient function notifies the QoS subsystem to stop tracking a client that has previously used the QOSStartTrackingClient function. If a flow is currently in progress, this function will not affect it.
helpviewer_keywords: ["QOSStopTrackingClient","QOSStopTrackingClient function [QOS]","qos.qosstoptrackingclient","qos2/QOSStopTrackingClient"]
old-location: qos\qosstoptrackingclient.htm
tech.root: QOS
ms.assetid: 7db9971e-3b53-458e-81ff-94f355c49973
ms.date: 12/05/2018
ms.keywords: QOSStopTrackingClient, QOSStopTrackingClient function [QOS], qos.qosstoptrackingclient, qos2/QOSStopTrackingClient
req.header: qos2.h
req.include-header: Qos2.h
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
req.lib: Qwave.lib
req.dll: Qwave.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QOSStopTrackingClient
 - qos2/QOSStopTrackingClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - qwave.dll
api_name:
 - QOSStopTrackingClient
---

# QOSStopTrackingClient function


## -description

The <b>QOSStopTrackingClient</b> function notifies the QoS subsystem to stop tracking a client that has previously used the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosstarttrackingclient">QOSStartTrackingClient</a> function. If a flow is currently in progress, this function will not affect it.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param DestAddr [in]

Pointer to a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that contains the IP address of the client device.  Clients are identified by their IP address and address family.  A port number is not required and will be ignored.

### -param Flags

Reserved for future use.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0.  To get extended error information, call <b>GetLastError</b>.  Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>QOSHandle</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>DestAddr</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Indicates that a memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are insufficient resources to carry out the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The request could not be performed because of an I/O device error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_REINITIALIZATION_NEEDER</b></dt>
</dl>
</td>
<td width="60%">
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ADAP_HDW_ERR</b></dt>
</dl>
</td>
<td width="60%">
A network adapter hardware error occurred.

</td>
</tr>
</table>

## -remarks

The Winsock2.h header file must be included to use Winsock defined identifiers or functions.


#### Examples

The following code shows this function called in an application setting.  See <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosstarttrackingclient">QOSStartTrackingClient</a> for parameter information.


```cpp
if(!QOSStopTrackingClient(QoSHandle, (sockaddr*)ptr->ai_addr, 0))
{
    std::cerr << std::endl;
    std::cerr << __FILE__ <<" Line: " << __LINE__ ;
    std::cerr << " - QOSStartTrackingClient failed. Exception code: "; 
    std::cerr << GetLastError() ;
}
else
{
    std::cout << "QoS client tracking stopped." << std::endl;
}


```

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosstarttrackingclient">QOSStartTrackingClient</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>