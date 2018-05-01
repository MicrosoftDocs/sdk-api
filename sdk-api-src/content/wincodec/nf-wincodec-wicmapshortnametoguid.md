---
UID: NF:wincodec.WICMapShortNameToGuid
title: WICMapShortNameToGuid function
author: windows-driver-content
description: Obtains the GUID associated with the given short name.
old-location: wic\_wic_codec_wicmapshortnametoguid.htm
old-project: wic
ms.assetid: ceefa802-7930-4b01-b1a2-6db530032e88
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: WICMapShortNameToGuid, WICMapShortNameToGuid function [Windows Imaging Component], _wic_codec_wicmapshortnametoguid, wic._wic_codec_wicmapshortnametoguid, wincodec/WICMapShortNameToGuid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Windowscodecs.dll
-	Wincodec.lib
api_name:
-	WICMapShortNameToGuid
product: Windows
targetos: Windows
req.lib: 
req.dll: Windowscodecs.dll; Wincodec.lib
req.irql: 
req.product: Windows Address Book 5.0
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

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can extend the short name mapping by adding to  the following registry key:


<pre xml:space="preserve"><b>HKEY_CLASSES_ROOT</b>
   <b>CLSID</b>
      <b>{FAE3D380-FEA4-4623-8C75-C6B61110B681}</b>
         <b>Namespace</b>
            <b>...</b></pre>


For more information, see <a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled Codec</a>.



