---
UID: NF:dwrite_3.IDWriteFactory3.GetSystemFontCollection
title: IDWriteFactory3::GetSystemFontCollection
author: windows-sdk-content
description: Retrieves a weight/width/slope tree of system fonts.
old-location: directwrite\idwritefactory3_getsystemfontcollection.htm
tech.root: DirectWrite
ms.assetid: f6e983b5-5c5f-a2de-59f8-722f967bb992
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetSystemFontCollection, GetSystemFontCollection method [Direct Write], GetSystemFontCollection method [Direct Write],IDWriteFactory3 interface, IDWriteFactory3 interface [Direct Write],GetSystemFontCollection method, IDWriteFactory3.GetSystemFontCollection, IDWriteFactory3::GetSystemFontCollection, directwrite.idwritefactory3_getsystemfontcollection, dwrite_3/IDWriteFactory3::GetSystemFontCollection
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
 - IDWriteFactory3.GetSystemFontCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory3::GetSystemFontCollection


## -description


Retrieves a weight/width/slope tree of system fonts.


## -parameters




### -param includeDownloadableFonts

Type: <b>BOOL</b>

Indicates whether to include cloud fonts or only locally installed fonts.

Type: <b>BOOL</b>

If this parameter is TRUE, the function performs an immediate check for changes       
           to the set of system fonts. If this parameter is FALSE, the function will still detect changes if the font      
           cache service is running, but there may be some latency. For example, an application might specify TRUE if      
           it has just installed a font and wants to be sure the font collection contains that font.


### -param fontCollection

Type: <b><a href="https://msdn.microsoft.com/bdee031b-53fa-321d-5cdc-4cc2c7ec58ca">IDWriteFontCollection1</a>**</b>

Holds the newly created font collection object, or NULL in case of failure.


### -param checkForUpdates

TBD




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/CCE68F89-6945-40F4-9C27-285AC8AB4D0B">IDWriteFactory3</a>
 

 

