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

# _SE_OBJECT_TYPE enumeration


## -description


The <b>SE_OBJECT_TYPE</b> enumeration contains values that correspond to the types of Windows objects that support security. The functions, such as 
<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a> and 
<a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a>, that set and retrieve the security information of an object, use these values to indicate the type of object.


## -enum-fields




### -field SE_UNKNOWN_OBJECT_TYPE

Unknown object type.


### -field SE_FILE_OBJECT

Indicates a file or directory. The name string that identifies a file or directory object can be in one of the following formats:

<ul>
<li>A relative path, such as <i>FileName.dat</i> or ..\<i>FileName</i></li>
<li>An absolute path, such as <i>FileName.dat</i>, C:\<i>DirectoryName</i>\<i>FileName.dat</i>, or G:\<i>RemoteDirectoryName</i>\<i>FileName.dat</i>.</li>
<li>A UNC name, such as \\<i>ComputerName</i>\<i>ShareName</i>\<i>FileName.dat</i>.</li>
</ul>

### -field SE_SERVICE

Indicates a Windows service. A service object can be a local service, such as <i>ServiceName</i>, or a remote service, such as \\<i>ComputerName</i>\<i>ServiceName</i>.


### -field SE_PRINTER

Indicates a printer. A printer object can be a local printer, such as <i>PrinterName</i>, or a remote printer, such as \\<i>ComputerName</i>\<i>PrinterName</i>.


### -field SE_REGISTRY_KEY

Indicates a registry key. A registry key object can be in the local registry, such as <b>CLASSES_ROOT</b>\<i>SomePath</i> or in a remote registry, such as \\<i>ComputerName</i>\<b>CLASSES_ROOT</b>\<i>SomePath</i>. 




The names of registry keys must use the following literal strings to identify the predefined registry keys: "CLASSES_ROOT", "CURRENT_USER", "MACHINE", and "USERS".


### -field SE_LMSHARE

Indicates a network share. A share object can be local, such as <i>ShareName</i>, or remote, such as \\<i>ComputerName</i>\<i>ShareName</i>.


### -field SE_KERNEL_OBJECT

Indicates a local 
<a href="https://msdn.microsoft.com/3e3288dd-155a-41d0-9d43-5f49ed4c4a9d">kernel object</a>. 




The 
<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a> and 
<a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a> functions support all types of kernel objects. The 
<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a> and 
<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a> functions work only with the following kernel objects: semaphore, event, mutex, waitable timer, and file mapping.


### -field SE_WINDOW_OBJECT

Indicates a window station or desktop object on the local computer. You cannot use 
<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a> and 
<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a> with these objects because the names of window stations or desktops are not unique.


### -field SE_DS_OBJECT

Indicates a directory service object or a property set or property of a directory service object. 



								The name string for a directory service object must be  in <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.500</a> form, for example:

CN=<i>SomeObject</i>,OU=<i>ou2</i>,OU=<i>ou1</i>,DC=<i>DomainName</i>,DC=<i>CompanyName</i>,DC=com,O=internet


### -field SE_DS_OBJECT_ALL

Indicates a directory service object and all of its property sets and properties.
					


### -field SE_PROVIDER_DEFINED_OBJECT

Indicates a provider-defined object.
					


### -field SE_WMIGUID_OBJECT

Indicates a WMI object.
					


### -field SE_REGISTRY_WOW64_32KEY

Indicates an object for a registry entry under WOW64.
					


### -field SE_REGISTRY_WOW64_64KEY




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/11f2119b-5314-4fa1-8016-9c01f79d037d">GetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a>



<a href="https://msdn.microsoft.com/70fbba50-2576-4857-a955-119fb12bf7b6">SetNamedSecurityInfo</a>



<a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a>
 

 

