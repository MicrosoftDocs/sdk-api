---
UID: NF:rometadataapi.IMetaDataImport2.GetVersionString
title: IMetaDataImport2::GetVersionString
author: windows-sdk-content
description: Gets the version number of the runtime that was used to build the assembly.
old-location: winrt\imetadataimport2_getversionstring.htm
old-project: WinRT
ms.assetid: 9f04ee6f-4a7d-4cdb-868e-eec2e9f41678
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetVersionString, GetVersionString method [Windows Runtime], GetVersionString method [Windows Runtime],IMetaDataImport2 interface, IMetaDataImport2 interface [Windows Runtime],GetVersionString method, IMetaDataImport2.GetVersionString, IMetaDataImport2::GetVersionString, rometadataapi/IMetaDataImport2::GetVersionString, winrt.imetadataimport2_getversionstring
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
 - IMetaDataImport2.GetVersionString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport2::GetVersionString


## -description


Gets the version number of the runtime that was used to build the assembly.


## -parameters




### -param pwzBuf [out]

An array to store the string that specifies the version.


### -param ccBufSize [in]

The size, in wide characters, of the <i>pwzBuf</i> array.


### -param pccBufSize [out]

The number of wide characters, including a null terminator, returned in the <i>pwzBuf</i> array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>GetVersionString</b> method gets the built-for version of the current metadata scope. If the scope has never been saved, it will not have a built-for version, and an empty string will be returned.




## -see-also




<a href="https://msdn.microsoft.com/32c462e0-d4b8-44db-b24b-c86b46be85bf">IMetaDataImport2</a>
 

 

