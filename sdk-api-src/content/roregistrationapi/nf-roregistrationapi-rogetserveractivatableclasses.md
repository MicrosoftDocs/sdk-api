---
UID: NF:roregistrationapi.RoGetServerActivatableClasses
title: RoGetServerActivatableClasses function (roregistrationapi.h)
description: Retrieves the activatable classes that are registered for a given executable (EXE) server, which was registered under the package ID of the calling process.
helpviewer_keywords: ["RoGetServerActivatableClasses","RoGetServerActivatableClasses function [Windows Runtime]","roregistrationapi/RoGetServerActivatableClasses","winrt.rogetserveractivatableclasses"]
old-location: winrt\rogetserveractivatableclasses.htm
tech.root: WinRT
ms.assetid: 845AC938-DE04-4151-8500-B8657234201C
ms.date: 12/05/2018
ms.keywords: RoGetServerActivatableClasses, RoGetServerActivatableClasses function [Windows Runtime], roregistrationapi/RoGetServerActivatableClasses, winrt.rogetserveractivatableclasses
req.header: roregistrationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Runtimeobject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RoGetServerActivatableClasses
 - roregistrationapi/RoGetServerActivatableClasses
dev_langs:
 - c++
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
---

# RoGetServerActivatableClasses function


## -description

Retrieves the activatable classes that are  registered for a given executable (EXE) server, which was registered under the package ID of the calling process.

## -parameters

### -param serverName [in]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a></b>

The name of the server to retrieve class registrations for. This server name is passed on the command line when the server is activated.

### -param activatableClassIds [out]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>**</b>

A callee-allocated array of activatable class ID strings which the server is registered to serve. The strings must be released by the caller using the <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a> function. The buffer must then be released using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. The server (caller) is responsible for registering the activation factories for these classes.

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

Use the <b>RoGetServerActivatableClasses</b> function to retrieve the class names that the server is expected to serve. Get the details on the individual classes by calling the <a href="/windows/desktop/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration">RoGetActivatableClassRegistration</a> function on each class name individually.