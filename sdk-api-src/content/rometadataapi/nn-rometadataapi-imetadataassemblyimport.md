---
UID: NN:rometadataapi.IMetaDataAssemblyImport
title: IMetaDataAssemblyImport (rometadataapi.h)
description: Provides methods to access and examine the contents of an assembly manifest.
helpviewer_keywords: ["IMetaDataAssemblyImport","IMetaDataAssemblyImport interface [Windows Runtime]","IMetaDataAssemblyImport interface [Windows Runtime]","described","rometadataapi/IMetaDataAssemblyImport","winrt.imetadataassemblyimport"]
old-location: winrt\imetadataassemblyimport.htm
tech.root: WinRT
ms.assetid: c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c
ms.date: 12/05/2018
ms.keywords: IMetaDataAssemblyImport, IMetaDataAssemblyImport interface [Windows Runtime], IMetaDataAssemblyImport interface [Windows Runtime],described, rometadataapi/IMetaDataAssemblyImport, winrt.imetadataassemblyimport
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMetaDataAssemblyImport
 - rometadataapi/IMetaDataAssemblyImport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport
---

# IMetaDataAssemblyImport interface


## -description

Provides methods to access and examine the contents of an assembly manifest.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataAssemblyImport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMetaDataAssemblyImport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMetaDataAssemblyImport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-closeenum">CloseEnum</a>
</td>
<td align="left" width="63%">
Releases a reference to the specified enumeration instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-enumassemblyrefs">EnumAssemblyRefs</a>
</td>
<td align="left" width="63%">
Enumerates the mdAssemblyRef instances that are defined in the assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-enumexportedtypes">EnumExportedTypes</a>
</td>
<td align="left" width="63%">
Enumerates the exported types referenced in the assembly manifest in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-enumfiles">EnumFiles</a>
</td>
<td align="left" width="63%">
Enumerates the files referenced in the current assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-enummanifestresources">EnumManifestResources</a>
</td>
<td align="left" width="63%">
Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-findassembliesbyname">FindAssembliesByName</a>
</td>
<td align="left" width="63%">
Gets an array of assemblies with the specified name, using the standard rules employed by the common language runtime (CLR) for resolving references.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-findexportedtypebyname">FindExportedTypeByName</a>
</td>
<td align="left" width="63%">
Gets a pointer to an exported type, given its name and enclosing type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-findmanifestresourcebyname">FindManifestResourceByName</a>
</td>
<td align="left" width="63%">
Gets a pointer to the manifest resource with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-getassemblyfromscope">GetAssemblyFromScope</a>
</td>
<td align="left" width="63%">
Gets a pointer to the assembly in the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-getassemblyprops">GetAssemblyProps</a>
</td>
<td align="left" width="63%">
Releases a reference to the specified enumeration instance.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-getassemblyrefprops">GetAssemblyRefProps</a>
</td>
<td align="left" width="63%">
Gets the set of properties for the assembly reference with the specified metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-getexportedtypeprops">GetExportedTypeProps</a>
</td>
<td align="left" width="63%">
Gets the set of properties of the exported type with the specified metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-getfileprops">GetFileProps</a>
</td>
<td align="left" width="63%">
Gets the properties of the file with the specified metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadataassemblyimport-getmanifestresourceprops">GetManifestResourceProps</a>
</td>
<td align="left" width="63%">
Gets the set of properties of the manifest resource with the specified metadata signature.

</td>
</tr>
</table>

