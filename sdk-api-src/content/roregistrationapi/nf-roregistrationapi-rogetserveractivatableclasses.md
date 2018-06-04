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

# RoGetServerActivatableClasses function


## -description


Retrieves the activatable classes that are  registered for a given executable (EXE) server, which was registered under the package ID of the calling process.


## -parameters




### -param serverName [in]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a></b>

The name of the server to retrieve class registrations for. This server name is passed on the command line when the server is activated.


### -param activatableClassIds [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>**</b>

A callee-allocated array of activatable class ID strings which the server is registered to serve. The strings must be released by the caller using the <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a> function. The buffer must then be released using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. The server (caller) is responsible for registering the activation factories for these classes.


### -param count [out]

Type: <b>DWORD*</b>

The count of activatable class IDs returned in the <i>activatableClassIds</i> array.


## -returns



Type: <b>HRESULT</b>

The method returns <b>S_OK</b> on success, otherwise an error code, including the following. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
An empty server name is provided, the server is not registered, or no classes are registered for this server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The process does not have sufficient permissions to read this server’s registration.

</td>
</tr>
</table>
 




## -remarks



Use the <b>RoGetServerActivatableClasses</b> function to retrieve the class names that the server is expected to serve. Get the details on the individual classes by calling the <a href="https://msdn.microsoft.com/9D9B74C9-9D9A-4E10-A222-C8F3658F2C48">RoGetActivatableClassRegistration</a> function on each class name individually.



