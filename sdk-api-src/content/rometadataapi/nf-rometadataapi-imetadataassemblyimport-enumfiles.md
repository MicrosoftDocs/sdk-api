---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumFiles
title: IMetaDataAssemblyImport::EnumFiles
author: windows-sdk-content
description: Enumerates the files referenced in the current assembly manifest.
old-location: winrt\imetadataassemblyimport_enumfiles.htm
tech.root: WinRT
ms.assetid: 4039432e-bcf1-4460-8be7-9f02c250ecc6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumFiles, EnumFiles method [Windows Runtime], EnumFiles method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumFiles method, IMetaDataAssemblyImport.EnumFiles, IMetaDataAssemblyImport::EnumFiles, rometadataapi/IMetaDataAssemblyImport::EnumFiles, winrt.imetadataassemblyimport_enumfiles
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IMetaDataAssemblyImport.EnumFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataAssemblyImport::EnumFiles


## -description


Enumerates the files referenced in the current assembly manifest.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be a null value for the first call of this method.


### -param rFiles [out]

The array used to store the <b>mdFile</b> metadata tokens.


### -param cMax [in]

The maximum number of <b>mdFile</b> tokens that can be placed in <i>rFiles</i>.


### -param pcTokens [out]

The number of <b>mdFile</b> tokens actually placed in <i>rFiles</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumFiles</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

