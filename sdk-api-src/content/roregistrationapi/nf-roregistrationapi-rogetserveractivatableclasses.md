---
UID: NF:roregistrationapi.RoGetServerActivatableClasses
title: RoGetServerActivatableClasses function
author: windows-sdk-content
description: Retrieves the activatable classes that are registered for a given executable (EXE) server, which was registered under the package ID of the calling process.
old-location: winrt\rogetserveractivatableclasses.htm
old-project: WinRT
ms.assetid: 845AC938-DE04-4151-8500-B8657234201C
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: RoGetServerActivatableClasses, RoGetServerActivatableClasses function [Windows Runtime], roregistrationapi/RoGetServerActivatableClasses, winrt.rogetserveractivatableclasses
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roregistrationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - runtimeobject.lib
 - runtimeobject.dll
 - API-MS-Win-Core-WinRT-registration-l1-1-0.dll
 - ComBase.dll
api_name:
 - RoGetServerActivatableClasses
product: Windows
targetos: Windows
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



