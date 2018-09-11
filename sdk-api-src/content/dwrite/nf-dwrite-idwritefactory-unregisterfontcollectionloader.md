---
UID: NF:dwrite.IDWriteFactory.UnregisterFontCollectionLoader
title: IDWriteFactory::UnregisterFontCollectionLoader
author: windows-sdk-content
description: Unregisters a custom font collection loader that was previously registered using RegisterFontCollectionLoader.
old-location: directwrite\IDWriteFactory_UnregisterFontCollectionLoader.htm
tech.root: DirectWrite
ms.assetid: 6a8682e3-72de-4afd-b9db-ba9b0d79f195
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteFactory interface [Direct Write],UnregisterFontCollectionLoader method, IDWriteFactory.UnregisterFontCollectionLoader, IDWriteFactory::UnregisterFontCollectionLoader, UnregisterFontCollectionLoader, UnregisterFontCollectionLoader method [Direct Write], UnregisterFontCollectionLoader method [Direct Write],IDWriteFactory interface, directwrite.IDWriteFactory_UnregisterFontCollectionLoader, dwrite/IDWriteFactory::UnregisterFontCollectionLoader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFactory.UnregisterFontCollectionLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::UnregisterFontCollectionLoader


## -description


 Unregisters a custom font collection loader that was previously registered using <a href="https://msdn.microsoft.com/495f8f56-42b6-4731-a26e-5da2c56a28ed">RegisterFontCollectionLoader</a>.


## -parameters




### -param fontCollectionLoader

Type: <b><a href="https://msdn.microsoft.com/898645ce-4bd5-4491-a31c-f60a17578872">IDWriteFontCollectionLoader</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/898645ce-4bd5-4491-a31c-f60a17578872">IDWriteFontCollectionLoader</a> object to be unregistered.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

