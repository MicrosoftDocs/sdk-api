---
UID: NF:rometadataapi.IMetaDataAssemblyImport.EnumExportedTypes
title: IMetaDataAssemblyImport::EnumExportedTypes
author: windows-sdk-content
description: Enumerates the exported types referenced in the assembly manifest in the current metadata scope.
old-location: winrt\imetadataassemblyimport_enumexportedtypes.htm
old-project: WinRT
ms.assetid: 8274d8e3-bcfb-4560-b925-2fede03be4cd
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: EnumExportedTypes, EnumExportedTypes method [Windows Runtime], EnumExportedTypes method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],EnumExportedTypes method, IMetaDataAssemblyImport.EnumExportedTypes, IMetaDataAssemblyImport::EnumExportedTypes, rometadataapi/IMetaDataAssemblyImport::EnumExportedTypes, winrt.imetadataassemblyimport_enumexportedtypes
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
 - IMetaDataAssemblyImport.EnumExportedTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataAssemblyImport::EnumExportedTypes


## -description


Enumerates the exported types referenced in the assembly manifest in the current metadata scope.


## -parameters




### -param phEnum [in, out]

 A pointer to the enumerator. This must be a null value when the <b>EnumExportedTypes</b> method is called for the first time.


### -param rExportedTypes [out]

The enumeration of <b>mdExportedType</b> metadata tokens.


### -param cMax [in]

The maximum number of <b>mdExportedType</b> tokens that can be placed in the <i>rExportedTypes</i> array.




### -param pcTokens [out]

The number of <b>mdExportedType</b> tokens actually placed in <i>rExportedTypes</i>.




## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumExportedTypes</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcTokens</i> is set to zero.
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

