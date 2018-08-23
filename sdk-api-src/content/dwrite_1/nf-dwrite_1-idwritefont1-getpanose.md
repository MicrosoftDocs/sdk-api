---
UID: NF:dwrite_1.IDWriteFont1.GetPanose
title: IDWriteFont1::GetPanose
author: windows-sdk-content
description: Gets the PANOSE values from the font and is used for font selection and matching.
old-location: directwrite\idwritefont1_getpanose.htm
old-project: DirectWrite
ms.assetid: DD31C1D6-4CD2-4ED0-BF9F-CAF587C613E6
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetPanose, GetPanose method [Direct Write], GetPanose method [Direct Write],IDWriteFont1 interface, IDWriteFont1 interface [Direct Write],GetPanose method, IDWriteFont1.GetPanose, IDWriteFont1::GetPanose, directwrite.idwritefont1_getpanose, dwrite_1/IDWriteFont1::GetPanose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite_1.dll
api_name:
 - IDWriteFont1.GetPanose
product: Windows
targetos: Windows
req.lib: Dwrite_1.lib
req.dll: Dwrite_1.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFont1::GetPanose


## -description


Gets the PANOSE values from the font and is used for font selection and
    matching.


## -parameters




### -param panose [out]

Type: <b><a href="https://msdn.microsoft.com/B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A">DWRITE_PANOSE</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A">DWRITE_PANOSE</a> structure to fill in.


## -returns



This method does not return a value.




## -remarks



If the font has no PANOSE values,
    they are set to 'any' (0) and <a href="https://msdn.microsoft.com/62a8d723-ae1c-4cbc-a9da-3177e80d4a3a">DirectWrite</a> doesn't simulate those values.




## -see-also




<a href="https://msdn.microsoft.com/50165292-8C5F-4FD2-A16B-9B8D9DB72F98">IDWriteFont1</a>
 

 

