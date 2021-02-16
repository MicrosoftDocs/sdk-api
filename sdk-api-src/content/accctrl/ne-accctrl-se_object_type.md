---
UID: NE:accctrl._SE_OBJECT_TYPE
title: SE_OBJECT_TYPE (accctrl.h)
description: Contains values that correspond to the types of Windows objects that support security.
helpviewer_keywords: ["SE_DS_OBJECT","SE_DS_OBJECT_ALL","SE_FILE_OBJECT","SE_KERNEL_OBJECT","SE_LMSHARE","SE_OBJECT_TYPE","SE_OBJECT_TYPE enumeration [Security]","SE_PRINTER","SE_PROVIDER_DEFINED_OBJECT","SE_REGISTRY_KEY","SE_REGISTRY_WOW64_32KEY","SE_SERVICE","SE_UNKNOWN_OBJECT_TYPE","SE_WINDOW_OBJECT","SE_WMIGUID_OBJECT","_win32_se_object_type_str","accctrl/SE_DS_OBJECT","accctrl/SE_DS_OBJECT_ALL","accctrl/SE_FILE_OBJECT","accctrl/SE_KERNEL_OBJECT","accctrl/SE_LMSHARE","accctrl/SE_OBJECT_TYPE","accctrl/SE_PRINTER","accctrl/SE_PROVIDER_DEFINED_OBJECT","accctrl/SE_REGISTRY_KEY","accctrl/SE_REGISTRY_WOW64_32KEY","accctrl/SE_SERVICE","accctrl/SE_UNKNOWN_OBJECT_TYPE","accctrl/SE_WINDOW_OBJECT","accctrl/SE_WMIGUID_OBJECT","security.se_object_type"]
old-location: security\se_object_type.htm
tech.root: security
ms.assetid: 1dee5e3d-0d41-4717-811b-7e05b4deb55f
ms.date: 12/05/2018
ms.keywords: SE_DS_OBJECT, SE_DS_OBJECT_ALL, SE_FILE_OBJECT, SE_KERNEL_OBJECT, SE_LMSHARE, SE_OBJECT_TYPE, SE_OBJECT_TYPE enumeration [Security], SE_PRINTER, SE_PROVIDER_DEFINED_OBJECT, SE_REGISTRY_KEY, SE_REGISTRY_WOW64_32KEY, SE_SERVICE, SE_UNKNOWN_OBJECT_TYPE, SE_WINDOW_OBJECT, SE_WMIGUID_OBJECT, _win32_se_object_type_str, accctrl/SE_DS_OBJECT, accctrl/SE_DS_OBJECT_ALL, accctrl/SE_FILE_OBJECT, accctrl/SE_KERNEL_OBJECT, accctrl/SE_LMSHARE, accctrl/SE_OBJECT_TYPE, accctrl/SE_PRINTER, accctrl/SE_PROVIDER_DEFINED_OBJECT, accctrl/SE_REGISTRY_KEY, accctrl/SE_REGISTRY_WOW64_32KEY, accctrl/SE_SERVICE, accctrl/SE_UNKNOWN_OBJECT_TYPE, accctrl/SE_WINDOW_OBJECT, accctrl/SE_WMIGUID_OBJECT, security.se_object_type
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: SE_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SE_OBJECT_TYPE
 - accctrl/_SE_OBJECT_TYPE
 - SE_OBJECT_TYPE
 - accctrl/SE_OBJECT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - SE_OBJECT_TYPE
---

# SE_OBJECT_TYPE enumeration


## -description

The <b>SE_OBJECT_TYPE</b> enumeration contains values that correspond to the types of Windows objects that support security. The functions, such as 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a>, that set and retrieve the security information of an object, use these values to indicate the type of object.

## -enum-fields

### -field SE_UNKNOWN_OBJECT_TYPE

Unknown object type.

### -field SE_FILE_OBJECT

Indicates a file or directory. The name string that identifies a file or directory object can be in one of the following formats:

<ul>
<li>A relative path, such as <i>FileName.dat</i> or ..&#92;<i>FileName</i></li>
<li>An absolute path, such as <i>FileName.dat</i>, C:&#92;<i>DirectoryName</i>&#92;<i>FileName.dat</i>, or G:&#92;<i>RemoteDirectoryName</i>&#92;<i>FileName.dat</i>.</li>
<li>A UNC name, such as &#92;&#92;<i>ComputerName</i>&#92;<i>ShareName</i>&#92;<i>FileName.dat</i>.</li>
</ul>

### -field SE_SERVICE

Indicates a Windows service. A service object can be a local service, such as <i>ServiceName</i>, or a remote service, such as &#92;&#92;<i>ComputerName</i>&#92;<i>ServiceName</i>.

### -field SE_PRINTER

Indicates a printer. A printer object can be a local printer, such as <i>PrinterName</i>, or a remote printer, such as &#92;&#92;<i>ComputerName</i>&#92;<i>PrinterName</i>.

### -field SE_REGISTRY_KEY

Indicates a registry key. A registry key object can be in the local registry, such as <b>CLASSES_ROOT</b>&#92;<i>SomePath</i> or in a remote registry, such as &#92;&#92;<i>ComputerName</i>&#92;<b>CLASSES_ROOT</b>&#92;<i>SomePath</i>. 




The names of registry keys must use the following literal strings to identify the predefined registry keys: "CLASSES_ROOT", "CURRENT_USER", "MACHINE", and "USERS".

### -field SE_LMSHARE

Indicates a network share. A share object can be local, such as <i>ShareName</i>, or remote, such as &#92;&#92;<i>ComputerName</i>&#92;<i>ShareName</i>.

### -field SE_KERNEL_OBJECT

Indicates a local 
<a href="/windows/desktop/SysInfo/kernel-objects">kernel object</a>. 




The 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> functions support all types of kernel objects. The 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a> functions work only with the following kernel objects: semaphore, event, mutex, waitable timer, and file mapping.

### -field SE_WINDOW_OBJECT

Indicates a window station or desktop object on the local computer. You cannot use 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a> with these objects because the names of window stations or desktops are not unique.

### -field SE_DS_OBJECT

Indicates a directory service object or a property set or property of a directory service object. 

The name string for a directory service object must be  in <a href="/windows/desktop/SecGloss/x-gly">X.500</a> form, for example:

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

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa">GetNamedSecurityInfo</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa">SetNamedSecurityInfo</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a>