---
UID: NF:dwrite_3.IDWriteFontFace3.GetPanose
title: IDWriteFontFace3::GetPanose
author: windows-sdk-content
description: Gets the PANOSE values from the font, used for font selection and matching.
old-location: directwrite\idwritefontface3_getpanose.htm
tech.root: DirectWrite
ms.assetid: 977AFC97-9747-4FCE-861E-E1C40975B2E9
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPanose, GetPanose method [Direct Write], GetPanose method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],GetPanose method, IDWriteFontFace3.GetPanose, IDWriteFontFace3::GetPanose, directwrite.idwritefontface3_getpanose, dwrite_3/IDWriteFontFace3::GetPanose
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
 - IDWriteFontFace3.GetPanose
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
- IDWriteFontFace3.GetPanose
: 
---

# IDWriteFontFace3::GetPanose


## -description


Gets the PANOSE values from the font, used for font selection and matching.


## -parameters




### -param panose [out]

Type: <b><a href="https://msdn.microsoft.com/B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A">DWRITE_PANOSE</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A">DWRITE_PANOSE</a> structure that receives the PANOSE values from the font.


## -returns



This method does not return a value.




## -remarks



This method doesn't simulate these values, such as substituting a weight or proportion inferred on other values. If the font doesn't specify them, they are all set to 'any' (0).




## -see-also




<a href="https://msdn.microsoft.com/1081A005-E4A8-4EE0-AFE0-10BD8D8471DF">IDWriteFontFace3</a>
 

 

