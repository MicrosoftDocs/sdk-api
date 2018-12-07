---
UID: NF:rometadataapi.IMetaDataImport.GetParamForMethodIndex
title: IMetaDataImport::GetParamForMethodIndex
author: windows-sdk-content
description: Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.
old-location: winrt\imetadataimport_getparamformethodindex.htm
tech.root: WinRT
ms.assetid: 118a5ab3-b7db-4e0c-bf45-ab7e2e0e4f03
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetParamForMethodIndex, GetParamForMethodIndex method [Windows Runtime], GetParamForMethodIndex method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetParamForMethodIndex method, IMetaDataImport.GetParamForMethodIndex, IMetaDataImport::GetParamForMethodIndex, rometadataapi/IMetaDataImport::GetParamForMethodIndex, winrt.imetadataimport_getparamformethodindex
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
 - IMetaDataImport.GetParamForMethodIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::GetParamForMethodIndex


## -description


Gets the token that represents a specified parameter of the method represented by the specified MethodDef token.


## -parameters




### -param tkMethodDef [in]

A token that represents the method to return the parameter token for.


### -param ulParamSeq [in]

The ordinal position in the parameter list where the requested parameter occurs. Parameters are numbered starting from one, with the method's return value in position zero.


### -param ptkParamDef [out]

A pointer to a ParamDef token that represents the requested parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

