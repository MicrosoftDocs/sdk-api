---
UID: NF:rometadataapi.IMetaDataImport.CountEnum
title: IMetaDataImport::CountEnum (rometadataapi.h)
author: windows-sdk-content
description: Gets the number of elements in the enumeration that was retrieved by the specified enumerator.
old-location: winrt\imetadataimport_countenum.htm
tech.root: WinRT
ms.assetid: 67146070-1710-4602-845c-a2a3cd5efdad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CountEnum, CountEnum method [Windows Runtime], CountEnum method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],CountEnum method, IMetaDataImport.CountEnum, IMetaDataImport::CountEnum, rometadataapi/IMetaDataImport::CountEnum, winrt.imetadataimport_countenum
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
 - IMetaDataImport.CountEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::CountEnum


## -description


Gets the number of elements in the enumeration that was retrieved by the specified enumerator.


## -parameters




### -param hEnum [in]

The handle for the enumerator.


### -param pulCount [out, retval]

The number of elements enumerated.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The handle specified by <i>hEnum</i> is obtained from a previous <b>Enum</b><i>Name</i> call (for example, <a href="https://msdn.microsoft.com/64dc7018-721f-4747-b798-fbf70bac18d5">IMetaDataImport::EnumTypeDefs</a>).




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

