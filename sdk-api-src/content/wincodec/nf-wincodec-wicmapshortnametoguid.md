---
UID: NF:wincodec.WICMapShortNameToGuid
title: WICMapShortNameToGuid function (wincodec.h)
description: Obtains the GUID associated with the given short name.
helpviewer_keywords: ["WICMapShortNameToGuid","WICMapShortNameToGuid function [Windows Imaging Component]","_wic_codec_wicmapshortnametoguid","wic._wic_codec_wicmapshortnametoguid","wincodec/WICMapShortNameToGuid"]
old-location: wic\_wic_codec_wicmapshortnametoguid.htm
tech.root: wic
ms.assetid: ceefa802-7930-4b01-b1a2-6db530032e88
ms.date: 12/05/2018
ms.keywords: WICMapShortNameToGuid, WICMapShortNameToGuid function [Windows Imaging Component], _wic_codec_wicmapshortnametoguid, wic._wic_codec_wicmapshortnametoguid, wincodec/WICMapShortNameToGuid
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
 - WICMapShortNameToGuid
 - wincodec/WICMapShortNameToGuid
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
 - WICMapShortNameToGuid
---

# WICMapShortNameToGuid function


## -description

Obtains the GUID associated with the given short name.

## -parameters

### -param wzName [in]

Type: <b>const WCHAR*</b>

A pointer to the short name.

### -param pguid [out]

Type: <b>GUID*</b>

A pointer that receives the GUID associated with the given short name.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can extend the short name mapping by adding to  the following registry key:


<pre><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{FAE3D380-FEA4-4623-8C75-C6B61110B681}</b>
         <b>Namespace</b>
            <b>...</b></pre>


For more information, see <a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled Codec</a>.
