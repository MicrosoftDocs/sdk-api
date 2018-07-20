---
UID: NF:rometadataapi.IMetaDataImport.GetScopeProps
title: IMetaDataImport::GetScopeProps
author: windows-sdk-content
description: Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.
old-location: winrt\imetadataimport_getscopeprops.htm
old-project: WinRT
ms.assetid: e7c7cc92-fa0e-426d-b26d-d8f87bffad7d
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetScopeProps, GetScopeProps method [Windows Runtime], GetScopeProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetScopeProps method, IMetaDataImport.GetScopeProps, IMetaDataImport::GetScopeProps, rometadataapi/IMetaDataImport::GetScopeProps, winrt.imetadataimport_getscopeprops
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
 - IMetaDataImport.GetScopeProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::GetScopeProps


## -description


Gets the name and optionally the version identifier of the assembly or module in the current metadata scope.


## -parameters




### -param szName [out]

A buffer for the assembly or module name.


### -param cchName [in]

The size in wide characters of <i>szName</i>.


### -param pchName [out]

The number of wide characters returned in <i>szName</i>.


### -param pmvid [out]

A pointer to a GUID that uniquely identifies the version of the assembly or module.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

