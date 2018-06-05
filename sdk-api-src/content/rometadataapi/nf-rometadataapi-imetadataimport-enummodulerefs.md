---
UID: NF:rometadataapi.IMetaDataImport.EnumModuleRefs
title: IMetaDataImport::EnumModuleRefs
author: windows-sdk-content
description: Enumerates ModuleRef tokens that represent imported modules.
old-location: winrt\imetadataimport_enummodulerefs.htm
old-project: WinRT
ms.assetid: dd3a8242-0cc9-4199-ada3-de227fe292bd
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: EnumModuleRefs, EnumModuleRefs method [Windows Runtime], EnumModuleRefs method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],EnumModuleRefs method, IMetaDataImport.EnumModuleRefs, IMetaDataImport::EnumModuleRefs, rometadataapi/IMetaDataImport::EnumModuleRefs, winrt.imetadataimport_enummodulerefs
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataImport.EnumModuleRefs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataImport::EnumModuleRefs


## -description


Enumerates ModuleRef tokens that represent imported modules.


## -parameters




### -param phEnum [in, out]

A pointer to the enumerator. This must be NULL for the first call of this method.


### -param rgModuleRefs [out]

The array used to store the ModuleRef tokens.


### -param cMax [in]

The maximum size of the <i>rgModuleRefs</i> array.


### -param pcModuleRefs [out]

The number of ModuleRef tokens returned in <i>rgModuleRefs</i>.


## -returns



<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td><b>S_OK</b></td>
<td><b>EnumModuleRefs</b> returned successfully.</td>
</tr>
<tr>
<td><b>S_FALSE</b></td>
<td>There are no tokens to enumerate. In this case, <i>pcModuleRefs</i> is 0 (zero).
 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

