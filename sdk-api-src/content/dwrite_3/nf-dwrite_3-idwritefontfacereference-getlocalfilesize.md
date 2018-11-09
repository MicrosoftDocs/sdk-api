---
UID: NF:dwrite_3.IDWriteFontFaceReference.GetLocalFileSize
title: IDWriteFontFaceReference::GetLocalFileSize
author: windows-sdk-content
description: Get the local size of the font face in bytes, which will always be less than or equal to GetFullSize. If the locality is remote, this value is zero. If full, this value will equal GetFileSize.
old-location: directwrite\idwritefontfacereference_getlocalfilesize.htm
tech.root: DirectWrite
ms.assetid: f6dc5cf5-131f-a451-7979-3ae8613577bb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetLocalFileSize, GetLocalFileSize method [Direct Write], GetLocalFileSize method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],GetLocalFileSize method, IDWriteFontFaceReference.GetLocalFileSize, IDWriteFontFaceReference::GetLocalFileSize, directwrite.idwritefontfacereference_getlocalfilesize, dwrite_3/IDWriteFontFaceReference::GetLocalFileSize
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
 - IDWriteFontFaceReference.GetLocalFileSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFaceReference::GetLocalFileSize


## -description


Get the local size of the font face in bytes, which will always be   
   less than or equal to GetFullSize. If the locality is remote, this     
   value is zero. If full, this value will equal GetFileSize.


## -parameters






## -returns



Type: <b>UINT64</b>

the local size of the font face in bytes, which will always be   
     less than or equal to GetFullSize. If the locality is remote, this     
     value is zero. If full, this value will equal <a href="https://msdn.microsoft.com/7988e724-2ccb-b182-8262-dacee1aa1f96">GetFileSize</a>.




## -see-also




<a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>
 

 

