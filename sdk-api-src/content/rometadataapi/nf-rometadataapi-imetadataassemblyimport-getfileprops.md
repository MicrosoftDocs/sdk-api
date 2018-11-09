---
UID: NF:rometadataapi.IMetaDataAssemblyImport.GetFileProps
title: IMetaDataAssemblyImport::GetFileProps
author: windows-sdk-content
description: Gets the properties of the file with the specified metadata signature.
old-location: winrt\imetadataassemblyimport_getfileprops.htm
tech.root: WinRT
ms.assetid: 28c884de-3b3c-48cd-9f6f-b2d56005de13
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetFileProps, GetFileProps method [Windows Runtime], GetFileProps method [Windows Runtime],IMetaDataAssemblyImport interface, IMetaDataAssemblyImport interface [Windows Runtime],GetFileProps method, IMetaDataAssemblyImport.GetFileProps, IMetaDataAssemblyImport::GetFileProps, rometadataapi/IMetaDataAssemblyImport::GetFileProps, winrt.imetadataassemblyimport_getfileprops
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
 - IMetaDataAssemblyImport.GetFileProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataAssemblyImport::GetFileProps


## -description


Gets the properties of the file with the specified metadata signature.


## -parameters




### -param mdf [in]

The <b>mdFile</b> metadata token that represents the file for which to get the properties.


### -param szName [out]

The simple name of the file.


### -param cchName [in]

The size, in wide chars, of <i>szName</i>.


### -param pchName [out]

The number of wide chars actually returned in <i>szName</i>.


### -param ppbHashValue [out]

A pointer to the hash value. This is the hash, using the SHA-1 algorithm, of the file.


### -param pcbHashValue [out]

The number of wide chars in the returned hash value.


### -param pdwFileFlags [out]

A pointer to the flags that describe the metadata applied to a file. The flags value is a combination of one or more <a href="http://msdn.microsoft.com/en-us/library/ms232970.aspx">CorFileFlags</a> values.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c4ae6028-87ac-4bb9-8eda-c6a48e5ecd3c">IMetaDataAssemblyImport</a>
 

 

