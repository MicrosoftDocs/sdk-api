---
UID: NE:wincodecsdk.WICPersistOptions
title: WICPersistOptions (wincodecsdk.h)
author: windows-sdk-content
description: Specifies Windows Imaging Component (WIC) options that are used when initializing a component with a stream.
old-location: wic\_wic_codec_wicpersistoptions.htm
tech.root: wic
ms.assetid: 8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WICPersistOptionBigEndian, WICPersistOptionDefault, WICPersistOptionLittleEndian, WICPersistOptionMask, WICPersistOptionNoCacheStream, WICPersistOptionPreferUTF8, WICPersistOptionStrictFormat, WICPersistOptions, WICPersistOptions enumeration [Windows Imaging Component], _wic_codec_wicpersistoptions, wic._wic_codec_wicpersistoptions, wincodecsdk/WICPersistOptionBigEndian, wincodecsdk/WICPersistOptionDefault, wincodecsdk/WICPersistOptionLittleEndian, wincodecsdk/WICPersistOptionMask, wincodecsdk/WICPersistOptionNoCacheStream, wincodecsdk/WICPersistOptionPreferUTF8, wincodecsdk/WICPersistOptionStrictFormat, wincodecsdk/WICPersistOptions
ms.topic: enum
f1_keywords: ["wincodecsdk/WICPersistOptions"]
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - HeaderDef
api_location:
 - Wincodecsdk.h
api_name:
 - WICPersistOptions
product: Windows
targetos: Windows
req.typenames: WICPersistOptions
req.redist: 
ms.custom: 19H1
---

# WICPersistOptions enumeration


## -description


Specifies Windows Imaging Component (WIC) options that are used when initializing a component with a stream.


## -enum-fields




### -field WICPersistOptionDefault

The default persist options. The default is <b>WICPersistOptionLittleEndian</b>.


### -field WICPersistOptionLittleEndian

The data byte order is little endian.


### -field WICPersistOptionBigEndian

The data byte order is big endian.


### -field WICPersistOptionStrictFormat

The data format must strictly conform to the specification.

<div class="alert"><b>Warning</b>  This option is inconsistently implement and should not be relied on.</div>
<div> </div>

### -field WICPersistOptionNoCacheStream

No cache for the metadata stream.

Certain operations, such as <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader">IWICComponentFactory::CreateMetadataWriterFromReader</a> require that the reader have a stream. Therefore, these operations will be unavailable if the reader is initialized with <b>WICPersistOptionNoCacheStream</b>.


### -field WICPersistOptionPreferUTF8

Use UTF8 instead of the default UTF16.

<div class="alert"><b>Note</b>  This option is currently unused by WIC.</div>
<div> </div>

### -field WICPersistOptionMask

The <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicpersistoptions">WICPersistOptions</a> mask.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicstreamprovider-getpersistoptions">GetPersistOptions</a>
 

 

