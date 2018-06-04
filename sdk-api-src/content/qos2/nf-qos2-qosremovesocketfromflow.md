---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# QOSRemoveSocketFromFlow function


## -description


The <b>QOSRemoveSocketFromFlow</b> function notifies the QOS subsystem that a previously added flow has been terminated by the application, and that the subsystem must update its internal information accordingly.


## -parameters




### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a>.


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
The indicated device requires reinitialization due to hardware errors. The application should clean up and call <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a> again.

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



Calling the  <a href="https://msdn.microsoft.com/e9e8e467-616c-419e-952d-2c9e93044a2f">QOSCloseHandle</a> function immediately aborts all pending operations and flows added by that handle.  If a handle is closed while a <b>QOSRemoveSocketFromFlow</b> call is still progress, the call will complete with <b>ERROR_OPERATION_ABORTED</b>.


#### Examples

The following code snippet demonstrates the use of <b>QOSRemoveSocketFromFlow</b>,  <a href="https://msdn.microsoft.com/e9e8e467-616c-419e-952d-2c9e93044a2f">QOSStopTrackingClient</a>, and <b>QOSCloseHandle</b> in an application function used for "cleaning up" QoS resources. See  <a href="https://msdn.microsoft.com/dcee0bed-dc6f-435d-b292-07e331f6cf5b">QOSCreateHandle</a> function for information on initialization of parameters. 

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2

<div class="alert"><b>Note</b>  The winsock2.h header file must be included to use WSAGetLastError and other Winsock functions.</div>
<div> </div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>int CleanUpQos( HANDLE qosHandle, 
            SOCKET connSocket, 
            QOS_FLOWID qosFlowId, 
            DWORD qosFlags,
            addrinfo *ptrAdrinfo) // qosFlags must be 0 
{

    int result = 0;
    BOOL removeStatus = FALSE;
 
    // The global variable gblClientTracking would be set on successful 
    // call to the QOSStartTrackingClient function.   
    if(gblClientTracking == TRUE &amp;&amp; qosHandle != NULL)
    {
        if(!QOSStopTrackingClient(qosHandle, (sockaddr*)ptrAdrinfo-&gt;ai_addr, 0))
        {
            gblClientTracking = FALSE;
            std::cerr &lt;&lt; std::endl;
            std::cerr &lt;&lt; __FILE__ &lt;&lt;" Line: " &lt;&lt; __LINE__ ;
            std::cerr &lt;&lt; " - QOSStartTrackingClient failed. Exception code: "; 
            std::cerr &lt;&lt; GetLastError() ;
        }
        else
        {
            std::cout &lt;&lt; "QoS client tracking stopped." &lt;&lt; std::endl;
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

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

