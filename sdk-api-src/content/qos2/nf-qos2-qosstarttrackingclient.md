---
UID: NF:qos2.QOSStartTrackingClient
title: QOSStartTrackingClient function (qos2.h)
description: The QOSStartTrackingClient function notifies the QOS subsystem of the existence of a new client.
helpviewer_keywords: ["QOSStartTrackingClient","QOSStartTrackingClient function [QOS]","qos.qosstarttrackingclient","qos2/QOSStartTrackingClient"]
old-location: qos\qosstarttrackingclient.htm
tech.root: QOS
ms.assetid: 36e4a71f-fb6b-42b6-a770-8cbcf98e7eb3
ms.date: 12/05/2018
ms.keywords: QOSStartTrackingClient, QOSStartTrackingClient function [QOS], qos.qosstarttrackingclient, qos2/QOSStartTrackingClient
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
 - QOSStartTrackingClient
 - qos2/QOSStartTrackingClient
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
 - QOSStartTrackingClient
---

# QOSStartTrackingClient function


## -description

The <b>QOSStartTrackingClient</b> function notifies the QOS subsystem of the existence of a new client. Calling this function increases the likelihood that the QOS subsystem will have gathered sufficient information on the network path to assist when calling <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a> to set the flow. <div class="alert"><b>Note</b>  This call is not required to add a flow with the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosaddsockettoflow">QOSAddSocketToFlow</a> function although it is highly recommended.  Not calling this function may require network experiments to be started during the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a> call and can result in <b>QOSSetFlow</b> failing with <b>ERROR_NETWORK_BUSY</b> on initial use.</div>
<div> </div>

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param DestAddr [in]

A pointer to a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure that contains the IP address of the client device.  Clients are identified by their IP address and address family.  Any port number specified in the sockaddr structure will be ignored.

### -param Flags

Reserved for future use.  Must be set to 0.

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
<dt><b>ERROR_DEVICE_REINITIALIZATION_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_HOST_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
The network location cannot be reached.

</td>
</tr>
</table>

## -remarks

On receipt of a <b>QOSStartTrackingClient</b> call the QoS subsystem begins gathering information about the client such as the QoS capabilities and available bandwidth on the end-to-end path.

An application should call this function as soon as it becomes aware of a client device that may need QoS flow.  For example this function should be called when a media player device first connects to a media server application.

Network experiments performed by <b>QOSStartTrackingClient</b> do not introduce noteworthy load on the network even if no stream is started for a long period of time.  The qWAVE service dynamically adjusts experiment traffic based on QoS subsystem activity.

Link Layer Topology Discovery (LLTD) must be implemented on the sink PC or device for this function to work.


#### Examples

The following code illustrates function use, handling a common exception, and required parameter initializations. Actual parameter values can vary depending on QoS version. The Winsock2.h header file must be included to use Winsock defined identifiers or functions.


```cpp
QOS_VERSION    Version;
HANDLE         QoSHandle = NULL;
BOOL        QoSResult = FALSE;

Version.MajorVersion = 1;
Version.MinorVersion = 0;

// Get a handle to the QoS subsystem (required for tracking).
QoSResult = QOSCreateHandle(
    &Version, 
    &QoSHandle );

if(!QOSStartTrackingClient(QoSHandle, (sockaddr*)ptr->ai_addr, 0))
{
    std::cerr << std::endl;
    std::cerr << __FILE__ <<" Line: " << __LINE__ ;
    std::cerr << " - QOSStartTrackingClient failed. Exception code: "; 
    std::cerr << GetLastError();

    if (GetLastError() == ERROR_NOT_SUPPORTED)
    {
        std::cerr << std::endl;
        std::cerr << " ERROR_NOT_SUPPORTED" << std::endl;
        std::cerr << "This operation requires information";
        std::cerr << "that the QoS subsystem does not have. " << std::endl;
    }
}
else
    std::cout << "QoS client tracking started." << std::endl;



```

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>