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

# IMetaDataImport::GetPinvokeMap


## -description


Gets a ModuleRef token to represent the target assembly of a PInvoke call.


## -parameters




### -param tk [in]

A FieldDef or MethodDef token to get the PInvoke mapping metadata for.


### -param pdwMappingFlags [out]

A pointer to flags used for mapping. This value is a bitmask from the <a href="http://msdn.microsoft.com/en-us/library/ms233461.aspx">CorPinvokeMap</a> enumeration.


### -param szImportName [out]

The name of the unmanaged target DLL.


### -param cchImportName [in]

The size in wide characters of <i>szImportName</i>.


### -param pchImportName [out]

The number of wide characters returned in <i>szImportName</i>.


### -param ptkImportDLL [out]

A pointer to a ModuleRef token that represents the unmanaged target object library.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

