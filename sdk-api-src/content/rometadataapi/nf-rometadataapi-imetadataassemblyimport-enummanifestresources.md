---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumManifestResources
title: IMetaDataAssemblyImport::EnumManifestResources
author: windows-sdk-content
description: Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.
old-location: winrt\imetadataassemblyimport_enummanifestresources.htm
old-project: WinRT
ms.assetid: 294ba92f-b6ef-4a66-81b5-b9ff508e147e
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: EnumManifestResources, EnumManifestResources method [Windows Runtime], EnumManifestResources method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumManifestResources method, IMetaDataAssemblyImport.EnumManifestResources, IMetaDataAssemblyImport::EnumManifestResources, rometadataapi/IMetaDataAssemblyImport::EnumManifestResources, winrt.imetadataassemblyimport_enummanifestresources
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataAssemblyImport.EnumManifestResources
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataAssemblyImport::EnumManifestResources


## -description


Gets a pointer to an enumerator for the resources referenced in the current assembly manifest.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be a null value when the <b>EnumManifestResources</b> method is called for the first time.




### -param rManifestResources [out]

The array used to store the <b>mdManifestResource</b> metadata tokens.


### -param cMax [in]

The maximum number of <b>mdManifestResource</b> tokens that can be placed in <i>rManifestResources</i>.


### -param pcTokens [out]

The number of <b>mdManifestResource</b> tokens actually placed in <i>rManifestResources</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumManifestResources</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

