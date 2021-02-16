---
UID: NS:winsxs._FUSION_INSTALL_REFERENCE_
title: FUSION_INSTALL_REFERENCE (winsxs.h)
description: The FUSION_INSTALL_REFERENCE structure contains information about the application which references the side-by-side assembly.
helpviewer_keywords: ["*LPFUSION_INSTALL_REFERENCE","FUSION_INSTALL_REFERENCE","FUSION_INSTALL_REFERENCE","FUSION_INSTALL_REFERENCE structure [Side-by-side Assemblies]","FUSION_REFCOUNT_FILEPATH_GUID","FUSION_REFCOUNT_MSI_GUID","FUSION_REFCOUNT_OPAQUE_STRING_GUID","FUSION_REFCOUNT_OSINSTALL_GUID","FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID","LPFUSION_INSTALL_REFERENCE","LPFUSION_INSTALL_REFERENCE structure pointer [Side-by-side Assemblies]","setup.fusion_install_reference_","winsxs/FUSION_INSTALL_REFERENCE","winsxs/LPFUSION_INSTALL_REFERENCE"]
old-location: setup\fusion_install_reference_.htm
tech.root: setup
ms.assetid: daa2b625-1522-4239-9c62-65f09b50f74c
ms.date: 12/05/2018
ms.keywords: '*LPFUSION_INSTALL_REFERENCE, FUSION_INSTALL_REFERENCE, FUSION_INSTALL_REFERENCE , FUSION_INSTALL_REFERENCE structure [Side-by-side Assemblies], FUSION_REFCOUNT_FILEPATH_GUID, FUSION_REFCOUNT_MSI_GUID, FUSION_REFCOUNT_OPAQUE_STRING_GUID, FUSION_REFCOUNT_OSINSTALL_GUID, FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID, LPFUSION_INSTALL_REFERENCE, LPFUSION_INSTALL_REFERENCE structure pointer [Side-by-side Assemblies], setup.fusion_install_reference_, winsxs/FUSION_INSTALL_REFERENCE, winsxs/LPFUSION_INSTALL_REFERENCE'
req.header: winsxs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FUSION_INSTALL_REFERENCE, *LPFUSION_INSTALL_REFERENCE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FUSION_INSTALL_REFERENCE_
 - winsxs/_FUSION_INSTALL_REFERENCE_
 - LPFUSION_INSTALL_REFERENCE
 - winsxs/LPFUSION_INSTALL_REFERENCE
 - FUSION_INSTALL_REFERENCE
 - winsxs/FUSION_INSTALL_REFERENCE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsxs.h
api_name:
 - FUSION_INSTALL_REFERENCE
---

# FUSION_INSTALL_REFERENCE structure


## -description

The <b>FUSION_INSTALL_REFERENCE</b> structure contains information about the application which references the side-by-side assembly. The assembly being referenced can be added to or removed from the side-by-side assembly store using the <a href="/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-installassembly">InstallAssembly</a> and <a href="/windows/desktop/api/winsxs/nf-winsxs-iassemblycache-uninstallassembly">UninstallAssembly</a> methods.

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
The assembly is referenced by an application that has been installed by using the <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a>. The <b>szIdentifier</b> member is set to MSI, and <b>szNonCannonicalData</b> is set to Windows Installer. Use this value for Windows side-by-side assemblies.

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