---
UID: NF:rometadataapi.IMetaDataImport.GetInterfaceImplProps
title: IMetaDataImport::GetInterfaceImplProps (rometadataapi.h)
description: Gets a pointer to the metadata tokens for the Type that implements the specified method, and for the interface that declares that method.
helpviewer_keywords: ["GetInterfaceImplProps","GetInterfaceImplProps method [Windows Runtime]","GetInterfaceImplProps method [Windows Runtime]","IMetaDataImport interface","IMetaDataImport interface [Windows Runtime]","GetInterfaceImplProps method","IMetaDataImport.GetInterfaceImplProps","IMetaDataImport::GetInterfaceImplProps","rometadataapi/IMetaDataImport::GetInterfaceImplProps","winrt.imetadataimport_getinterfaceimplprops"]
old-location: winrt\imetadataimport_getinterfaceimplprops.htm
tech.root: WinRT
ms.assetid: ff91bb07-8e3a-49f1-9cd6-1c3e18a3c242
ms.date: 12/05/2018
ms.keywords: GetInterfaceImplProps, GetInterfaceImplProps method [Windows Runtime], GetInterfaceImplProps method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetInterfaceImplProps method, IMetaDataImport.GetInterfaceImplProps, IMetaDataImport::GetInterfaceImplProps, rometadataapi/IMetaDataImport::GetInterfaceImplProps, winrt.imetadataimport_getinterfaceimplprops
f1_keywords:
- rometadataapi/IMetaDataImport.GetInterfaceImplProps
dev_langs:
- c++
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
- IMetaDataImport.GetInterfaceImplProps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataImport::GetInterfaceImplProps


## -description


Gets a pointer to the metadata tokens for the Type that implements the specified method, and for the interface that declares that method.


## -parameters




### -param tkInterfaceImpl [in]

The metadata token representing the method to return the class and interface tokens for.


### -param ptkClass [out]

The metadata token representing the class that implements the method.


### -param ptkIface [out]

The metadata token representing the interface that defines the implemented method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadataimport">IMetaDataImport</a>
 

 

