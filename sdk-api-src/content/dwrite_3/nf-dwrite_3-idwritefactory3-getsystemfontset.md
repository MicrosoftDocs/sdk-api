---
UID: NF:dwrite_3.IDWriteFactory3.GetSystemFontSet
title: IDWriteFactory3::GetSystemFontSet
author: windows-sdk-content
description: Retrieves the list of system fonts.
old-location: directwrite\idwritefactory3_getsystemfontset.htm
tech.root: DirectWrite
ms.assetid: 84fd8c9f-f4b1-3015-f431-08b7a07ff32b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetSystemFontSet, GetSystemFontSet method [Direct Write], GetSystemFontSet method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],GetSystemFontSet method, IDWriteFactory3.GetSystemFontSet, IDWriteFactory3::GetSystemFontSet, directwrite.idwritefactory3_getsystemfontset, dwrite_3/IDWriteFactory3::GetSystemFontSet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFactory3.GetSystemFontSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::GetSystemFontSet


## -description


Retrieves the list of system fonts.


## -parameters




### -param fontSet [out]

Type: <b><a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>**</b>

Holds the newly created font set object, or NULL in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

