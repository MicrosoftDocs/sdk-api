---
UID: NC:ws2spi.LPNSPGETSERVICECLASSINFO
title: LPNSPGETSERVICECLASSINFO
author: windows-sdk-content
description: Retrieves all the pertinent class information (schema) pertaining to the namespace provider.
old-location: winsock\nspgetserviceclassinfo_2.htm
tech.root: WinSock
ms.assetid: babe1c96-9077-4d91-a52a-839c89d7a83b
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: LPNSPGETSERVICECLASSINFO, NSPGetServiceClassInfo, NSPGetServiceClassInfo function [Winsock], _win32_nspgetserviceclassinfo_2, winsock.nspgetserviceclassinfo_2, ws2spi/NSPGetServiceClassInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ws2spi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - NSPGetServiceClassInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPNSPGETSERVICECLASSINFO callback function


## -description


The 
<b>NSPGetServiceClassInfo</b> function retrieves all the pertinent class information (schema) pertaining to the namespace provider. This call retrieves any namespace-specific information that is common to all instances of the service, including connection information for SAP, or port information for SAP or TCP.


## -parameters




### -param lpProviderId [in]

A pointer to the GUID of the specific namespace provider from which the service class schema is to be retrieved.


### -param lpdwBufSize [in, out]

On input, the size, in bytes, of the buffer pointed to by <i>lpServiceClassInfo</i> parameter. 

On output, if the function fails and the error is 
<a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a>, this parameter specifies the minimum size, in bytes, of the buffer pointed to the <i>lpServiceClassInfo</i> parameter needed to retrieve the record.


### -param lpServiceClassInfo [in, out]

Returns a pointer to <a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFOW</a> structure that contains the service class to namespace-specific mapping information. The <i>lpServiceClassId</i> parameter must be filled to indicate which <b>WSASERVICECLASSINFOW</b> record should be returned.


## -returns



If no error occurs, the 
<b>NSPGetServiceClassInfo</b> function returns <b>NO_ERROR</b> (zero). Otherwise, <b>SOCKET_ERROR</b> (–1) is returned and the namespace provider must set the appropriate error code using <a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSA_NOT_ENOUGH_MEMORY</a></b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEACCES</a></b></dt>
</dl>
</td>
<td width="60%">
The calling routine does not have sufficient privileges to access the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEFAULT</a></b></dt>
</dl>
</td>
<td width="60%">
The  buffer pointed to by the <i>lpServiceClass</i> parameter was too small to contain a <a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFOW</a> structure. The application needs to pass in a larger buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEINVAL</a></b></dt>
</dl>
</td>
<td width="60%">
The specified service class identifier or namespace provider identifier is not valid. This error is returned if the <i>lpProviderId</i>, <i>lpServiceClassId</i>, <i>lpdwBufSize</i>, or <i>lpServiceClassInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSAEOPNOTSUPP</a></b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported. This error is returned if the namespace provider does not implement this function. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSANO_DATA</a></b></dt>
</dl>
</td>
<td width="60%">
The requested name is valid, but no data of the requested type was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="https://msdn.microsoft.com/en-us/library/ms740668(v=VS.85).aspx">WSATYPE_NOT_FOUND</a></b></dt>
</dl>
</td>
<td width="60%">
The specified class was not found.

</td>
</tr>
</table>
 




## -remarks



The W2_32.dll uses this function to implement the 
<a href="https://msdn.microsoft.com/0a61751e-10e5-4f91-a0b2-8c1baf477653">WSAGetServiceClassNameByClassId</a> function, as well as to retrieve the namespace-specific information passed to the 
<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a> and 
<a href="https://msdn.microsoft.com/df76ea75-c0bc-48b8-b1a7-0c510c5cc28d">NSPSetService</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/437a3580-e296-4f20-8921-84e522cccc1a">NSPInstallServiceClass</a>



<a href="https://msdn.microsoft.com/a0b71821-4434-470f-b729-370d7e1722ec">NSPLookupServiceBegin</a>



<a href="https://msdn.microsoft.com/97313e6f-ec9e-4dcb-b888-14436259a519">NSPRemoveServiceClass</a>



<a href="https://msdn.microsoft.com/df76ea75-c0bc-48b8-b1a7-0c510c5cc28d">NSPSetService</a>



<a href="https://msdn.microsoft.com/e177bb7d-c7d3-43a4-a809-ab8212feea2e">WSAGetServiceClassInfo</a>



<a href="https://msdn.microsoft.com/0a61751e-10e5-4f91-a0b2-8c1baf477653">WSAGetServiceClassNameByClassId</a>



<a href="https://msdn.microsoft.com/02422c24-34a6-4e34-a795-66b0b687ac44">WSASERVICECLASSINFOW</a>



<a href="https://msdn.microsoft.com/596155ee-3dcc-4ae3-97ab-0653e019cbee">WSASetLastError</a>
 

 

