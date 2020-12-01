---
UID: NS:roparameterizediid.IRoMetaDataLocator
title: IRoMetaDataLocator (roparameterizediid.h)
description: Enables the RoGetParameterizedTypeInstanceIID function to access run-time metadata.
helpviewer_keywords: ["IRoMetaDataLocator","IRoMetaDataLocator structure [Windows Runtime]","PIRoMetaDataLocator","PIRoMetaDataLocator structure pointer [Windows Runtime]","roparameterizediid/IRoMetaDataLocator","roparameterizediid/PIRoMetaDataLocator","winrt.irometadatalocator_struct"]
old-location: winrt\irometadatalocator_struct.htm
tech.root: WinRT
ms.assetid: A1004454-1C9F-46AF-8C88-BB8204FA0410
ms.date: 12/05/2018
ms.keywords: IRoMetaDataLocator, IRoMetaDataLocator structure [Windows Runtime], PIRoMetaDataLocator, PIRoMetaDataLocator structure pointer [Windows Runtime], roparameterizediid/IRoMetaDataLocator, roparameterizediid/PIRoMetaDataLocator, winrt.irometadatalocator_struct
req.header: roparameterizediid.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRoMetaDataLocator
 - roparameterizediid/IRoMetaDataLocator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - roparameterizediid.h
api_name:
 - IRoMetaDataLocator
---

# IRoMetaDataLocator structure


## -description

Enables the <a href="/windows/desktop/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid">RoGetParameterizedTypeInstanceIID</a> function to access run-time metadata.

Implement <b>IRoMetaDataLocator</b> when you're implementing programming language bindings to enable a language to call Windows platform APIs by using Windows metadata (.winmd) files.

## -struct-fields

### -field Locate

Gets a metadata builder for the specified type.



#### nameElement

A Windows Runtime type or parameterized type to resolve.



#### metaDataDestination

A data sink for Windows Runtime metadata. The caller should invoke the appropriate set method to provide the metadata for the type named by <i>nameElement</i>.

## -see-also

<a href="/windows/desktop/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile">RoGetMetaDataFile</a>