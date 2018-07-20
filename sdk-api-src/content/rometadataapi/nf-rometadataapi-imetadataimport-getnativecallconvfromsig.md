---
UID: NF:rometadataapi.IMetaDataImport.GetNativeCallConvFromSig
title: IMetaDataImport::GetNativeCallConvFromSig
author: windows-sdk-content
description: Gets the native calling convention for the method that is represented by the specified signature pointer.
old-location: winrt\imetadataimport_getnativecallconvfromsig.htm
old-project: WinRT
ms.assetid: 90e09d3d-c77e-44c3-b4d0-6b2aee995b1e
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetNativeCallConvFromSig, GetNativeCallConvFromSig method [Windows Runtime], GetNativeCallConvFromSig method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetNativeCallConvFromSig method, IMetaDataImport.GetNativeCallConvFromSig, IMetaDataImport::GetNativeCallConvFromSig, rometadataapi/IMetaDataImport::GetNativeCallConvFromSig, winrt.imetadataimport_getnativecallconvfromsig
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
 - IMetaDataImport.GetNativeCallConvFromSig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMetaDataImport::GetNativeCallConvFromSig


## -description


Gets the native calling convention for the method that is represented by the specified signature pointer.


## -parameters




### -param pvSig




### -param cbSig [in]

The size in bytes of <i>const</i>.


### -param pCallConv [out]

A pointer to the native calling convention.


#### - const [in]

A pointer to the metadata signature of the method to return the calling convention for.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

