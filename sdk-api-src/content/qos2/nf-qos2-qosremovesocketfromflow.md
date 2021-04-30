---
UID: NF:qos2.QOSRemoveSocketFromFlow
title: QOSRemoveSocketFromFlow function (qos2.h)
description: Notifies the QOS subsystem that a previously added flow has been terminated.
helpviewer_keywords: ["QOSRemoveSocketFromFlow","QOSRemoveSocketFromFlow function [QOS]","qos.qosremovesocketfromflow","qos2/QOSRemoveSocketFromFlow"]
old-location: qos\qosremovesocketfromflow.htm
tech.root: QOS
ms.assetid: c67dc959-2511-4a95-87e4-1689f49c167a
ms.date: 12/05/2018
ms.keywords: QOSRemoveSocketFromFlow, QOSRemoveSocketFromFlow function [QOS], qos.qosremovesocketfromflow, qos2/QOSRemoveSocketFromFlow
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
 - QOSRemoveSocketFromFlow
 - qos2/QOSRemoveSocketFromFlow
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
 - QOSRemoveSocketFromFlow
---

# QOSRemoveSocketFromFlow function


## -description

The <b>QOSRemoveSocketFromFlow</b> function notifies the QOS subsystem that a previously added flow has been terminated by the application, and that the subsystem must update its internal information accordingly.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

### -param Socket [in, optional]

Socket to be removed from the flow.

Only flows created with the <b>QOS_NON_ADAPTIVE_FLOW</b> flag may have multiple sockets added to the same flow.  By passing the <i>Socket</i> parameter in this call, each socket can be removed individually.  If the <i>Socket</i> parameter is not passed, the entire flow will be destroyed.  If only one socket was attached to the flow, passing this socket as a parameter to this function and passing <b>NULL</b> as a socket are equivalent calls.

### -param FlowId [in]

A flow identifier. A <b>QOS_FLOWID</b> is an unsigned 32-bit integer.

### -param Flags

Reserved for future use. This parameter must be set to 0.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>FlowId</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are insufficient system resources to carry out the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPERATION_ABORTED</b></dt>
</dl>
</td>
<td width="60%">
The request was blocked.

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
<dt><b>ERROR_HOST_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
The network location cannot be reached.

</td>
</tr>
</table>

## -remarks

Calling the  <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosclosehandle">QOSCloseHandle</a> function immediately aborts all pending operations and flows added by that handle.  If a handle is closed while a <b>QOSRemoveSocketFromFlow</b> call is still progress, the call will complete with <b>ERROR_OPERATION_ABORTED</b>.


#### Examples

The following code snippet demonstrates the use of <b>QOSRemoveSocketFromFlow</b>,  <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosclosehandle">QOSStopTrackingClient</a>, and <b>QOSCloseHandle</b> in an application function used for "cleaning up" QoS resources. See  <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> function for information on initialization of parameters. 

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2

<div class="alert"><b>Note</b>  The winsock2.h header file must be included to use WSAGetLastError and other Winsock functions.</div>
<div> </div>

```cpp
int CleanUpQos( HANDLE qosHandle, 
            SOCKET connSocket, 
            QOS_FLOWID qosFlowId, 
            DWORD qosFlags,
            addrinfo *ptrAdrinfo) // qosFlags must be 0 
{

    int result = 0;
    BOOL removeStatus = FALSE;
 
    // The global variable gblClientTracking would be set on successful 
    // call to the QOSStartTrackingClient function.   
    if(gblClientTracking == TRUE && qosHandle != NULL)
    {
        if(!QOSStopTrackingClient(qosHandle, (sockaddr*)ptrAdrinfo->ai_addr, 0))
        {
            gblClientTracking = FALSE;
            std::cerr << std::endl;
            std::cerr << __FILE__ <<" Line: " << __LINE__ ;
            std::cerr << " - QOSStartTrackingClient failed. Exception code: "; 
            std::cerr << GetLastError() ;
        }
        else
        {
            std::cout << "QoS client tracking stopped." << std::endl;
        }
    }

    if (qosFlowId != 0 )
    {
        if( QOSRemoveSocketFromFlow(
                qosHandle,
                connSocket,
                qosFlowId,
                qosFlags) != TRUE)
        {        
            result = WSAGetLastError();
        }
        else
        {
            // Mutex + Wait function would provide additional protection 
            // against the possibility of ERROR_OPERATION_ABORTED exception.     
            if( QOSCloseHandle(qosHandle) != TRUE)
                result = WSAGetLastError();
        }
    }

    return(result);
}


```

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>