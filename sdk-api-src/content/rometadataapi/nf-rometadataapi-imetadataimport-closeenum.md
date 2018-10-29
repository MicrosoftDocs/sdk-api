---
UID: NF:rometadataapi.IMetaDataImport.CloseEnum
title: IMetaDataImport::CloseEnum
author: windows-sdk-content
description: Closes the enumerator that is identified by the specified handle.
old-location: winrt\imetadataimport_closeenum.htm
tech.root: WinRT
ms.assetid: 3495afdf-ca88-4967-b7b3-6320114b9c50
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CloseEnum, CloseEnum method [Windows Runtime], CloseEnum method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],CloseEnum method, IMetaDataImport.CloseEnum, IMetaDataImport::CloseEnum, rometadataapi/IMetaDataImport::CloseEnum, winrt.imetadataimport_closeenum
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
 - IMetaDataImport.CloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::CloseEnum


## -description


Closes the enumerator that is identified by the specified handle.


## -parameters




### -param hEnum [in]

The handle of the enumerator to close.


## -returns



This method does not return a value.




## -remarks



The handle specified by <i>hEnum</i> is obtained from a previous <b>Enum</b><i>Name</i> call (for example, <a href="https://msdn.microsoft.com/64dc7018-721f-4747-b798-fbf70bac18d5">IMetaDataImport::EnumTypeDefs</a>).




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

