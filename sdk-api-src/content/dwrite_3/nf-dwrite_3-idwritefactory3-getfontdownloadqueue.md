---
UID: NF:dwrite_3.IDWriteFactory3.GetFontDownloadQueue
title: IDWriteFactory3::GetFontDownloadQueue
author: windows-sdk-content
description: Gets the font download queue associated with this factory object.
old-location: directwrite\idwritefactory3_getfontdownloadqueue.htm
tech.root: DirectWrite
ms.assetid: 446e4544-b25d-9b59-922c-ca5c896ea99f
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetFontDownloadQueue, GetFontDownloadQueue method [Direct Write], GetFontDownloadQueue method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],GetFontDownloadQueue method, IDWriteFactory3.GetFontDownloadQueue, IDWriteFactory3::GetFontDownloadQueue, directwrite.idwritefactory3_getfontdownloadqueue, dwrite_3/IDWriteFactory3::GetFontDownloadQueue
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
 - IDWriteFactory3.GetFontDownloadQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_3.h
: 
- IDWriteFactory3.GetFontDownloadQueue
: 
---

# IDWriteFactory3::GetFontDownloadQueue


## -description


Gets the font download queue associated with this factory object.


## -parameters




### -param fontDownloadQueue [out]

Type: <b><a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>**</b>

Receives a pointer to the font download queue interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

