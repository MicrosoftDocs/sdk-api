---
UID: NF:rometadataapi.IMetaDataImport.GetMethodSemantics
title: IMetaDataImport::GetMethodSemantics
author: windows-sdk-content
description: Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.
old-location: winrt\imetadataimport_getmethodsemantics.htm
tech.root: WinRT
ms.assetid: b4133bf8-4ae4-43ad-8d07-4f7805e9ef2c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetMethodSemantics, GetMethodSemantics method [Windows Runtime], GetMethodSemantics method [Windows Runtime],IMetaDataImport interface, IMetaDataImport interface [Windows Runtime],GetMethodSemantics method, IMetaDataImport.GetMethodSemantics, IMetaDataImport::GetMethodSemantics, rometadataapi/IMetaDataImport::GetMethodSemantics, winrt.imetadataimport_getmethodsemantics
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
 - IMetaDataImport.GetMethodSemantics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMetaDataImport::GetMethodSemantics


## -description


Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.


## -parameters




### -param tkMethodDef [in]

A MethodDef token representing the method to get the semantic role information for.


### -param tkEventProp [in]

A token representing the paired property and event for which to get the method's role.


### -param pdwSemanticsFlags [out]

A pointer to the associated semantics flags. This value is a bitmask from the CorMethodSemanticsAttr enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5457d9d3-9a43-4e89-a52f-1254662ed92a">IMetaDataImport</a>
 

 

