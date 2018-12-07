---
UID: NF:dwrite_3.IDWriteRemoteFontFileLoader.GetLocalityFromKey
title: IDWriteRemoteFontFileLoader::GetLocalityFromKey
author: windows-sdk-content
description: Gets the locality of the file resource identified by the unique key.
old-location: directwrite\idwriteremotefontfileloader_getlocalityfromkey.htm
tech.root: DirectWrite
ms.assetid: 997D8F04-8667-4D90-B097-CD48F979BE02
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLocalityFromKey, GetLocalityFromKey method [Direct Write], GetLocalityFromKey method [Direct Write],IDWriteRemoteFontFileLoader interface, IDWriteRemoteFontFileLoader interface [Direct Write],GetLocalityFromKey method, IDWriteRemoteFontFileLoader.GetLocalityFromKey, IDWriteRemoteFontFileLoader::GetLocalityFromKey, directwrite.idwriteremotefontfileloader_getlocalityfromkey, dwrite_3/IDWriteRemoteFontFileLoader::GetLocalityFromKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteRemoteFontFileLoader.GetLocalityFromKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteRemoteFontFileLoader::GetLocalityFromKey


## -description


Gets the locality of the file resource identified by the unique key.


## -parameters




### -param fontFileReferenceKey [in]

Type: <b>void</b>

Font file reference key that uniquely identifies the font file resource within the scope of the font loader being used.


### -param fontFileReferenceKeySize

Type: <b>UINT32</b>

Size of font file reference key in bytes.


### -param locality [out]

Type: <b><a href="https://msdn.microsoft.com/DEBFE4E0-C995-4468-9702-44EA37F1BCFF">DWRITE_LOCALITY</a>*</b>

Locality of the file.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="https://msdn.microsoft.com/16CFF7ED-642A-48D8-8C72-3EC68B702E50">IDWriteRemoteFontFileLoader</a>
 

 

