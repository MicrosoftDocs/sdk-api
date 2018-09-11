---
UID: NF:dwrite_3.IDWriteFont3.GetLocality
title: IDWriteFont3::GetLocality
author: windows-sdk-content
description: Gets the current locality of the font.
old-location: directwrite\idwritefont3_getlocality.htm
tech.root: DirectWrite
ms.assetid: B7CD16AE-77A3-4C3C-91B7-3AD32DCF68C0
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetLocality, GetLocality method [Direct Write], GetLocality method [Direct Write],IDWriteFont3 interface, IDWriteFont3 interface [Direct Write],GetLocality method, IDWriteFont3.GetLocality, IDWriteFont3::GetLocality, directwrite.idwritefont3_getlocality, dwrite_3/IDWriteFont3::GetLocality
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
 - IDWriteFont3.GetLocality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont3::GetLocality


## -description


Gets the current locality of the font.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/DEBFE4E0-C995-4468-9702-44EA37F1BCFF">DWRITE_LOCALITY</a></b>

Returns the current locality of the font.




## -remarks



For fully local files, the result will always  be DWRITE_LOCALITY_LOCAL. A downloadable file may be any of the states, and this function may change between calls.




## -see-also




<a href="https://msdn.microsoft.com/0BD21E3C-5F02-4A51-B64C-847B0DD5656B">IDWriteFont3</a>
 

 

