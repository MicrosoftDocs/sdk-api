---
UID: NF:olectl.DllRegisterServer
title: DllRegisterServer function
author: windows-sdk-content
description: Instructs an in-process server to create its registry entries for all classes supported in this server module.
old-location: com\dllregisterserver.htm
tech.root: com
ms.assetid: 4442206b-b2ad-47d7-8add-18002c44c5a2
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: DllRegisterServer, DllRegisterServer function [COM], _com_DllRegisterServer, com.dllregisterserver, olectl/DllRegisterServer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: olectl.h
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - DllRegisterServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DllRegisterServer function


## -description


Instructs an in-process server to create its registry entries for all classes supported in this server module.


## -parameters






## -returns



This function can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The registry entries were created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SELFREG_E_TYPELIB</b></dt>
</dl>
</td>
<td width="60%">
The server was unable to complete the registration of all the type libraries used by its classes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SELFREG_E_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The server was unable to complete the registration of all the object classes.


</td>
</tr>
</table>
 




## -remarks



E_NOTIMPL is not a valid return code.

If this function fails, the state of the registry for all its classes is undefined.




## -see-also




<a href="https://msdn.microsoft.com/b71137a7-284e-4521-a3b2-9dad9c9d3c54">DllUnregisterServer</a>
 

 

