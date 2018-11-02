---
UID: NN:rometadataapi.IMetaDataAssemblyImport
title: IMetaDataAssemblyImport
author: windows-sdk-content
description: Provides methods to access and examine the contents of an assembly manifest.
old-location: winrt\imetadataassemblyimport.htm
tech.root: WinRT
ms.assetid: c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMetaDataAssemblyImport, IMetaDataAssemblyImport interface [Windows Runtime], IMetaDataAssemblyImport interface [Windows Runtime],described, rometadataapi/IMetaDataAssemblyImport, winrt.imetadataassemblyimport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataAssemblyImport interface


## -description


Provides methods to access and examine the contents of an assembly manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMetaDataAssemblyImport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMetaDataAssemblyImport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/95adc5b3-19f1-4be1-bb77-a481f81f5d3e">CloseEnum</a>
</td>
<td align="left" width="63%">
Releases a reference to the specified enumeration instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b5768ef-47fc-4052-bb68-e279a027c887">EnumAssemblyRefs</a>
</td>
<td align="left" width="63%">
Enumerates the mdAssemblyRef instances that are defined in the assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8274d8e3-bcfb-4560-b925-2fede03be4cd">EnumExportedTypes</a>
</td>
<td align="left" width="63%">
Enumerates the exported types referenced in the assembly manifest in the current metadata scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4039432e-bcf1-4460-8be7-9f02c250ecc6">EnumFiles</a>
</td>
<td align="left" width="63%">
Enumerates the files referenced in the current assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/294ba92f-b6ef-4a66-81b5-b9ff508e147e">EnumManifestResources</a>
</td>
<td align="left" width="63%">
Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/147158ba-060e-404e-9721-3d0c2498f5c9">FindAssembliesByName</a>
</td>
<td align="left" width="63%">
Gets an array of assemblies with the specified name, using the standard rules employed by the common language runtime (CLR) for resolving references.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b19b41c-fd1b-4284-8455-2b0d69907c99">FindExportedTypeByName</a>
</td>
<td align="left" width="63%">
Gets a pointer to an exported type, given its name and enclosing type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a72e4c1f-505d-4672-8baa-fbe2243b8ca0">FindManifestResourceByName</a>
</td>
<td align="left" width="63%">
Gets a pointer to the manifest resource with the specified name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7b7d650-2db6-4e7c-92e0-5d0055a0a5a9">GetAssemblyFromScope</a>
</td>
<td align="left" width="63%">
Gets a pointer to the assembly in the current scope.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f60657c-46b4-4491-a9e2-73868886f51d">GetAssemblyProps</a>
</td>
<td align="left" width="63%">
Releases a reference to the specified enumeration instance.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2a0d54f-dc9d-4c3c-80e7-725da985f23b">GetAssemblyRefProps</a>
</td>
<td align="left" width="63%">
Gets the set of properties for the assembly reference with the specified metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbdd4f9c-f070-463e-91af-4a7c6c6a45d2">GetExportedTypeProps</a>
</td>
<td align="left" width="63%">
Gets the set of properties of the exported type with the specified metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28c884de-3b3c-48cd-9f6f-b2d56005de13">GetFileProps</a>
</td>
<td align="left" width="63%">
Gets the properties of the file with the specified metadata signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caa859c8-de40-4de6-bf90-41104cef91b2">GetManifestResourceProps</a>
</td>
<td align="left" width="63%">
Gets the set of properties of the manifest resource with the specified metadata signature.

</td>
</tr>
</table> 

