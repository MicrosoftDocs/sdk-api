---
UID: NF:rometadataapi.IMetaDataDispenser.DefineScope
title: IMetaDataDispenser::DefineScope
author: windows-driver-content
description: Creates a new area in memory in which you can create new metadata.
old-location: winrt\imetadatadispenser_definescope.htm
old-project: WinRT
ms.assetid: 5b7a5e73-e7ef-427a-baa4-3f0defd566a3
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: DefineScope, DefineScope method [Windows Runtime], DefineScope method [Windows Runtime],IMetaDataDispenser interface, IMetaDataDispenser interface [Windows Runtime],DefineScope method, IMetaDataDispenser.DefineScope, IMetaDataDispenser::DefineScope, rometadataapi/IMetaDataDispenser::DefineScope, winrt.imetadatadispenser_definescope
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataDispenser.DefineScope
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataDispenser::DefineScope


## -description


Creates a new area in memory in which you can create new metadata.


## -parameters




### -param rclsid [in]

The CLSID of the version of metadata structures to be created.


### -param dwCreateFlags [in]

Flags that specify options.


### -param riid [in]

The IID of the desired metadata interface to be returned. The caller will use the interface to create the new metadata.

The value of riid must specify one of the "emit" interfaces. Valid values are <b>IID_IMetaDataEmit</b>, <b>IID_IMetaDataAssemblyEmit</b>, or <b>IID_IMetaDataEmit2</b>.




### -param ppIUnk [out]

The pointer to the returned interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>DefineScope</b> creates a set of in-memory metadata tables, generates a unique GUID (module version identifier, or MVID) for the metadata, and creates an entry in the module table for the compilation unit being emitted.




## -see-also




<a href="https://msdn.microsoft.com/3454193d-9068-4032-ae9e-b3087509b0b8">IMetaDataDispenser</a>
 

 

