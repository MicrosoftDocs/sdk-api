---
UID: NF:qos2.QOSCloseHandle
title: QOSCloseHandle function (qos2.h)
description: The QOSCloseHandle function closes a handle returned by the QOSCreateHandle function.
helpviewer_keywords: ["QOSCloseHandle","QOSCloseHandle function [QOS]","qos.qosclosehandle","qos2/QOSCloseHandle"]
old-location: qos\qosclosehandle.htm
tech.root: QOS
ms.assetid: e9e8e467-616c-419e-952d-2c9e93044a2f
ms.date: 12/05/2018
ms.keywords: QOSCloseHandle, QOSCloseHandle function [QOS], qos.qosclosehandle, qos2/QOSCloseHandle
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
 - QOSCloseHandle
 - qos2/QOSCloseHandle
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
 - QOSCloseHandle
---

# QOSCloseHandle function


## -description

The <b>QOSCloseHandle</b> function closes a handle returned by the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a> function.

## -parameters

### -param QOSHandle [in]

Handle to the QOS subsystem returned by <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qoscreatehandle">QOSCreateHandle</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0.  To get extended error information, call <b>GetLastError</b>.

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
The <i>QOSHandle</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

All flows added on the handle being closed are immediately removed from the system.  Any traffic going out of a socket used to create these flows will no longer be marked with priority values.  Any pending operations on these flows are immediately completed with <b>ERROR_ABORTED</b>.

If any clients were being tracked through the handle being closed by a previous call to the <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosstarttrackingclient">QOSStartTrackingClient</a> function, <b>QOSCloseHandle</b> indicates that the application is no longer using the client endpoint.


#### Examples

The following "CleanUpQos" function illustrates  the use of <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosremovesocketfromflow">QOSRemoveSocketFromFlow</a> and <b>QOSCloseHandle</b>:  

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2

The Winsock2.h header file must be included to use Winsock defined identifiers or functions.


```cpp
int CleanUpQos( HANDLE qosHandle, 
           SOCKET connSocket, 
           QOS_FLOWID qosFlowId, 
           DWORD qosFlags // qosFlags must be 0 
           )
{
  // To ensure against generating an ERROR_OPERATION_ABORTED exception
  // use a separate thread and Mutex protection to verify completion
  // of QOSRemoveSocketFromFlow before calling QOSCloseHandle.

  int result = 0;
   
  if (qosFlowId != 0)
  {
    if( QOSRemoveSocketFromFlow(
        qosHandle,
        connSocket,
        qosFlowId,
        qosFlags) != TRUE)
    
            result = WSAGetLastError();
  }

  // Under Mutex protection, add Wait function here. 

  if (qosHandle != NULL)
  {
    if( QOSCloseHandle(qosHandle) != TRUE)
        result = WSAGetLastError();
  }

  return(result);

}


```

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>