---
UID: NF:rometadataapi.IMetaDataImport.GetModuleRefProps
title: IMetaDataImport::GetModuleRefProps
author: windows-sdk-content
description: Gets the name of the module referenced by the specified metadata token.
old-location: winrt\imetadataimport_getmodulerefprops.htm
old-project: WinRT
ms.assetid: 1f14fe81-d585-4167-8817-0c7d000413de
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetModuleRefProps, GetModuleRefProps method [Windows Runtime], GetModuleRefProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetModuleRefProps method, IMetaDataImport.GetModuleRefProps, IMetaDataImport::GetModuleRefProps, rometadataapi/IMetaDataImport::GetModuleRefProps, winrt.imetadataimport_getmodulerefprops
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
 - IMetaDataImport.GetModuleRefProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::GetModuleRefProps


## -description


Gets the name of the module referenced by the specified metadata token.


## -parameters




### -param tkModuleRef [in]

The ModuleRef metadata token that references the module to get metadata information for.


### -param szName [out]

A buffer to hold the module name.


### -param cchName [in]

The requested size of <i>szName</i> in wide characters.


### -param pchName [out]

The returned size of <i>szName</i> in wide characters.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

