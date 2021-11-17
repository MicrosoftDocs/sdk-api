---
UID: NF:wincodec.WICMapSchemaToName
title: WICMapSchemaToName function (wincodec.h)
description: Obtains the name associated with a given schema.
helpviewer_keywords: ["WICMapSchemaToName","WICMapSchemaToName function [Windows Imaging Component]","_wic_codec_wicmapschematoname","wic._wic_codec_wicmapschematoname","wincodec/WICMapSchemaToName"]
old-location: wic\_wic_codec_wicmapschematoname.htm
tech.root: wic
ms.assetid: 6e71b75a-a542-459c-9935-b05f3ce39217
ms.date: 12/05/2018
ms.keywords: WICMapSchemaToName, WICMapSchemaToName function [Windows Imaging Component], _wic_codec_wicmapschematoname, wic._wic_codec_wicmapschematoname, wincodec/WICMapSchemaToName
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICMapSchemaToName
 - wincodec/WICMapSchemaToName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Windowscodecs.lib
api_name:
 - WICMapSchemaToName
---

# WICMapSchemaToName function


## -description

Obtains the name associated with a given schema.

## -parameters

### -param guidMetadataFormat [in]

Type: <b><a href="/windows/desktop/wic/-wic-guids-clsids">REFGUID</a></b>

The metadata format GUID.

### -param pwzSchema [in]

Type: <b>LPWSTR</b>

The URI string of the schema for which the name is to be retrieved.

### -param cchName [in]

Type: <b>UINT</b>

The size of the <i>wzName</i> buffer.

### -param wzName [in, out]

Type: <b>WCHAR*</b>

A pointer to a buffer that receives the schema's name.

To obtain the required buffer size, call <b>WICMapSchemaToName</b> with <i>cchName</i> set to 0 and <i>wzName</i> set to <b>NULL</b>.

### -param pcchActual [out]

Type: <b>UINT</b>

The actual buffer size needed to retrieve the entire schema name.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can extend the schema name mapping by adding to the following registry key:


<pre><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{FAE3D380-FEA4-4623-8C75-C6B61110B681}</b>
         <b>Schemas</b>
            <b>BB5ACC38-F216-4CEC-A6C5-5F6E739763A9</b>
               <b>...</b></pre>


For more information, see <a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled Codec</a>.
