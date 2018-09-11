---
UID: NF:qos2.QOSCreateHandle
title: QOSCreateHandle function
author: windows-sdk-content
description: This function initializes the QOS subsystem and the QOSHandle parameter. The QOSHandle parameter is used when calling other QOS functions. QOSCreateHandle must be called before any other functions.
old-location: qos\qoscreatehandle.htm
tech.root: QOS
ms.assetid: dcee0bed-dc6f-435d-b292-07e331f6cf5b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: QOSCreateHandle, QOSCreateHandle function [QOS], qos.qoscreatehandle, qos2/QOSCreateHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - qwave.dll
api_name:
 - QOSCreateHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QOSCreateHandle function


## -description


This function initializes the QOS subsystem and the <i>QOSHandle</i> parameter.  The  <i>QOSHandle</i> parameter is used when calling other QOS functions.  <b>QOSCreateHandle</b> must be called before any other functions.


<a href="https://msdn.microsoft.com/e9e8e467-616c-419e-952d-2c9e93044a2f">QOSCloseHandle</a> closes handles created by this function.


## -parameters




### -param Version [in]

Pointer to a <a href="https://msdn.microsoft.com/cc8d6dc3-87e9-46c7-8192-78053b4932a3">QOS_VERSION</a> structure that indicates the version of QOS being used.  The <b>MajorVersion</b> member must be set to 1, and the <b>MinorVersion</b> member must be set to 0.


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

If a machine enters a power save mode that interrupts connectivity such as sleep or standby, existing and active network experiments such as <a href="https://msdn.microsoft.com/36e4a71f-fb6b-42b6-a770-8cbcf98e7eb3">QOSStartTrackingClient</a> must be reinitiated.  This recreation of the flow mirrors the cleanup and creation activities also necessary for existing sockets. A new handle must be created, and the flow must be recreated and readmitted.


#### Examples

The following code illustrates function use and required parameter initializations. Actual values will vary depending on QoS version.

Winsock.h must be included to use the <a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a> function.

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




<a href="https://msdn.microsoft.com/022fde13-415e-49aa-8df4-472c4eadd6a0">Quality Windows Audio/Video Experience (qWAVE)</a>
 

 

