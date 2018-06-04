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

# _FUSION_INSTALL_REFERENCE_ structure


## -description


The <b>FUSION_INSTALL_REFERENCE</b> structure contains information about the application which references the side-by-side assembly. The assembly being referenced can be added to or removed from the side-by-side assembly store using the <a href="https://msdn.microsoft.com/aff1da20-9e82-43d5-b601-f73ee2dba0fe">InstallAssembly</a> and <a href="https://msdn.microsoft.com/b492e93c-73f2-4d68-ae1a-c82e9ec36a72">UninstallAssembly</a> methods.


## -struct-fields




### -field cbSize

The size of the structure in bytes.


### -field dwFlags

Reserved, this member must be zero.


### -field guidScheme

The application  that uses the side-by-side assembly.


 This parameter can have one of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FUSION_REFCOUNT_MSI_GUID"></a><a id="fusion_refcount_msi_guid"></a><dl>
<dt><b>FUSION_REFCOUNT_MSI_GUID</b></dt>
</dl>
</td>
<td width="60%">
The assembly is referenced by an application that has been installed by using the <a href="https://msdn.microsoft.com/c90b8cbe-d7a1-44ad-ae65-80115bd55e4f">Windows Installer</a>. The <b>szIdentifier</b> member is set to MSI, and <b>szNonCannonicalData</b> is set to Windows Installer. Use this value for Windows side-by-side assemblies.

</td>
</tr>
<tr>
<td width="40%"><a id="FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID"></a><a id="fusion_refcount_uninstall_subkey_guid"></a><dl>
<dt><b>FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID</b></dt>
</dl>
</td>
<td width="60%">
The assembly is referenced by an application that appears in Add/Remove Programs. The <b>szIdentifier</b> member is the token used to register the application with Add/Remove programs.

</td>
</tr>
<tr>
<td width="40%"><a id="FUSION_REFCOUNT_FILEPATH_GUID"></a><a id="fusion_refcount_filepath_guid"></a><dl>
<dt><b>FUSION_REFCOUNT_FILEPATH_GUID</b></dt>
</dl>
</td>
<td width="60%">
The assembly is referenced by an application that is represented by a file in the file system. The <b>szIdentifier</b> parameter is the path to this file.

</td>
</tr>
<tr>
<td width="40%"><a id="FUSION_REFCOUNT_OPAQUE_STRING_GUID"></a><a id="fusion_refcount_opaque_string_guid"></a><dl>
<dt><b>FUSION_REFCOUNT_OPAQUE_STRING_GUID</b></dt>
</dl>
</td>
<td width="60%">
The assembly is referenced by an application that is only represented by an opaque string. The <b>szIdentifier</b> member is this opaque string. This value is required for the side-by-side store to check for the existence of opaque references.

</td>
</tr>
<tr>
<td width="40%"><a id="FUSION_REFCOUNT_OSINSTALL_GUID"></a><a id="fusion_refcount_osinstall_guid"></a><dl>
<dt><b>FUSION_REFCOUNT_OSINSTALL_GUID</b></dt>
</dl>
</td>
<td width="60%">
Reserved

</td>
</tr>
</table>
 


### -field szIdentifier

A pointer to a string value that identifies the application that references assembly. The meaning of this identifier depends on the <b>guidScheme</b> parameter.


### -field szNonCannonicalData

A string that is used only by the application that reference the assembly.

