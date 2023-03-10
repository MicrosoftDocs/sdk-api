---
UID: NF:qos2.QOSCreateHandle
title: QOSCreateHandle function (qos2.h)
description: This function initializes the QOS subsystem and the QOSHandle parameter. The QOSHandle parameter is used when calling other QOS functions. QOSCreateHandle must be called before any other functions.
helpviewer_keywords: ["QOSCreateHandle","QOSCreateHandle function [QOS]","qos.qoscreatehandle","qos2/QOSCreateHandle"]
old-location: qos\qoscreatehandle.htm
tech.root: QOS
ms.assetid: dcee0bed-dc6f-435d-b292-07e331f6cf5b
ms.date: 12/05/2018
ms.keywords: QOSCreateHandle, QOSCreateHandle function [QOS], qos.qoscreatehandle, qos2/QOSCreateHandle
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
 - QOSCreateHandle
 - qos2/QOSCreateHandle
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
 - QOSCreateHandle
---

# QOSCreateHandle function


## -description

This function initializes the QOS subsystem and the <i>QOSHandle</i> parameter.  The  <i>QOSHandle</i> parameter is used when calling other QOS functions.  <b>QOSCreateHandle</b> must be called before any other functions.


<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosclosehandle">QOSCloseHandle</a> closes handles created by this function.

## -parameters

### -param Version [in]

Pointer to a <a href="/windows/desktop/api/qos2/ns-qos2-qos_version">QOS_VERSION</a> structure that indicates the version of QOS being used.  The <b>MajorVersion</b> member must be set to 1, and the <b>MinorVersion</b> member must be set to 0.

### -param QOSHandle [out]

Pointer to a variable that receives a QOS handle.  This handle is used when calling other QOS functions.

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
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
Internal logic error.  Initialization failed.  For example, if the host goes into sleep or standby mode, all existing handles and flows are rendered invalid.

</td>
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
<dt><b>ERROR_RESOURCE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
A resource required by the service is unavailable.  This error may be returned if the user has not enabled the firewall exception for the qWAVE service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_DEPENDENCY_FAIL</b></dt>
</dl>
</td>
<td width="60%">
One of the dependencies of this service is unavailable.  The qWAVE service could not be started.

</td>
</tr>
</table>

## -remarks

Every process intending to use qWAVE must first call <b>QOSCreateHandle</b>. The handle returned can be used for performing overlapped I/O. For example, this handle can be associated with an I/O completion port (IOCP) to receive overlapped completion notifications. This function can be  called multiple times to obtain multiple handles although a single handle is sufficient for most applications.

If a machine enters a power save mode that interrupts connectivity such as sleep or standby, existing and active network experiments such as <a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosstarttrackingclient">QOSStartTrackingClient</a> must be reinitiated.  This recreation of the flow mirrors the cleanup and creation activities also necessary for existing sockets. A new handle must be created, and the flow must be recreated and readmitted.


#### Examples

The following code illustrates function use and required parameter initializations. Actual values will vary depending on QoS version.

Winsock.h must be included to use the <a href="/windows/desktop/api/winsock/nf-winsock-wsagetlasterror">WSAGetLastError</a> function.

See the Windows SDK for a complete sample code listing. SDK folder: Samples\NetDs\GQos\Qos2


```cpp
QOS_VERSION Version;
HANDLE      QoSHandle = NULL;
BOOL        QoSResult = FALSE;

// Initialize the QoS version parameter.
Version.MajorVersion = 1;
Version.MinorVersion = 0;

// Get a handle to the QoS subsystem.
QoSResult = QOSCreateHandle(
    &Version, 
    &QoSHandle );

if (QoSResult != TRUE)
{
    std::cerr << "QOSCreateHandle failed. Error: "; 
    std::cerr << WSAGetLastError() << std::endl;
}



```

## -see-also

<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>