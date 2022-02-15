---
UID: NF:wincodec.WICMapGuidToShortName
title: WICMapGuidToShortName function (wincodec.h)
description: Obtains the short name associated with a given GUID.
helpviewer_keywords: ["WICMapGuidToShortName","WICMapGuidToShortName function [Windows Imaging Component]","_wic_codec_wicmapguidtoshortname","wic._wic_codec_wicmapguidtoshortname","wincodec/WICMapGuidToShortName"]
old-location: wic\_wic_codec_wicmapguidtoshortname.htm
tech.root: wic
ms.assetid: ae1e4680-2c20-4a3e-b931-206d26f4d09c
ms.date: 12/05/2018
ms.keywords: WICMapGuidToShortName, WICMapGuidToShortName function [Windows Imaging Component], _wic_codec_wicmapguidtoshortname, wic._wic_codec_wicmapguidtoshortname, wincodec/WICMapGuidToShortName
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
req.lib: WindowsCodecs.lib
req.dll: WindowsCodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WICMapGuidToShortName
 - wincodec/WICMapGuidToShortName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WindowsCodecs.dll
api_name:
 - WICMapGuidToShortName
---

# WICMapGuidToShortName function


## -description

Obtains the short name associated with a given GUID.

## -parameters

### -param guid [in]

Type: <b>REFGUID</b>

The GUID to retrieve the short name for.

### -param cchName [in]

Type: <b>UINT</b>

The size of the <i>wzName</i> buffer.

### -param wzName [in, out]

Type: <b>WCHAR*</b>

A pointer that receives the short name associated with the GUID.

### -param pcchActual [out]

Type: <b>UINT*</b>

The actual size needed to retrieve the entire short name associated with the GUID.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Windows Imaging Component (WIC) short name mappings can be found within the following registry key:
            <pre><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{FAE3D380-FEA4-4623-8C75-C6B61110B681}</b>
         <b>Namespace</b>
            <b>...</b></pre>

