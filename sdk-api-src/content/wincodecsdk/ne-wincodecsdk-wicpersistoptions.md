---
UID: NE:wincodecsdk.WICPersistOptions
title: WICPersistOptions (wincodecsdk.h)
description: Specifies Windows Imaging Component (WIC) options that are used when initializing a component with a stream.
helpviewer_keywords: ["WICPersistOptionBigEndian","WICPersistOptionDefault","WICPersistOptionLittleEndian","WICPersistOptionMask","WICPersistOptionNoCacheStream","WICPersistOptionPreferUTF8","WICPersistOptionStrictFormat","WICPersistOptions","WICPersistOptions enumeration [Windows Imaging Component]","_wic_codec_wicpersistoptions","wic._wic_codec_wicpersistoptions","wincodecsdk/WICPersistOptionBigEndian","wincodecsdk/WICPersistOptionDefault","wincodecsdk/WICPersistOptionLittleEndian","wincodecsdk/WICPersistOptionMask","wincodecsdk/WICPersistOptionNoCacheStream","wincodecsdk/WICPersistOptionPreferUTF8","wincodecsdk/WICPersistOptionStrictFormat","wincodecsdk/WICPersistOptions"]
old-location: wic\_wic_codec_wicpersistoptions.htm
tech.root: wic
ms.assetid: 8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6
ms.date: 12/05/2018
ms.keywords: WICPersistOptionBigEndian, WICPersistOptionDefault, WICPersistOptionLittleEndian, WICPersistOptionMask, WICPersistOptionNoCacheStream, WICPersistOptionPreferUTF8, WICPersistOptionStrictFormat, WICPersistOptions, WICPersistOptions enumeration [Windows Imaging Component], _wic_codec_wicpersistoptions, wic._wic_codec_wicpersistoptions, wincodecsdk/WICPersistOptionBigEndian, wincodecsdk/WICPersistOptionDefault, wincodecsdk/WICPersistOptionLittleEndian, wincodecsdk/WICPersistOptionMask, wincodecsdk/WICPersistOptionNoCacheStream, wincodecsdk/WICPersistOptionPreferUTF8, wincodecsdk/WICPersistOptionStrictFormat, wincodecsdk/WICPersistOptions
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
targetos: Windows
req.typenames: WICPersistOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICPersistOptions
 - wincodecsdk/WICPersistOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincodecsdk.h
api_name:
 - WICPersistOptions
---

# WICPersistOptions enumeration


## -description

Specifies Windows Imaging Component (WIC) options that are used when initializing a component with a stream.

## -enum-fields

### -field WICPersistOptionDefault:0

The default persist options. The default is <b>WICPersistOptionLittleEndian</b>.

### -field WICPersistOptionLittleEndian:0

The data byte order is little endian.

### -field WICPersistOptionBigEndian:0x1

The data byte order is big endian.

### -field WICPersistOptionStrictFormat:0x2

The data format must strictly conform to the specification.

<div class="alert"><b>Warning</b>  This option is inconsistently implement and should not be relied on.</div>
<div> </div>

### -field WICPersistOptionNoCacheStream:0x4

No cache for the metadata stream.

Certain operations, such as <a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader">IWICComponentFactory::CreateMetadataWriterFromReader</a> require that the reader have a stream. Therefore, these operations will be unavailable if the reader is initialized with <b>WICPersistOptionNoCacheStream</b>.

### -field WICPersistOptionPreferUTF8:0x8

Use UTF8 instead of the default UTF16.

<div class="alert"><b>Note</b>  This option is currently unused by WIC.</div>
<div> </div>

### -field WICPersistOptionMask:0xffff

The <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicpersistoptions">WICPersistOptions</a> mask.

## -see-also

<a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicstreamprovider-getpersistoptions">GetPersistOptions</a>
