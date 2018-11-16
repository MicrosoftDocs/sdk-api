---
UID: NF:dwrite_3.IDWriteFontFaceReference.CreateFontFaceWithSimulations
title: IDWriteFontFaceReference::CreateFontFaceWithSimulations
author: windows-sdk-content
description: Creates a font face with alternate font simulations, for example, to explicitly simulate a bold font face out of a regular variant.
old-location: directwrite\idwritefontfacereference_createfontfacewithsimulations.htm
tech.root: DirectWrite
ms.assetid: 99b6fb24-2f66-8132-b66e-ca711bb0c7e0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateFontFaceWithSimulations, CreateFontFaceWithSimulations method [Direct Write], CreateFontFaceWithSimulations method [Direct Write],IDWriteFontFaceReference interface, IDWriteFontFaceReference interface [Direct Write],CreateFontFaceWithSimulations method, IDWriteFontFaceReference.CreateFontFaceWithSimulations, IDWriteFontFaceReference::CreateFontFaceWithSimulations, directwrite.idwritefontfacereference_createfontfacewithsimulations, dwrite_3/IDWriteFontFaceReference::CreateFontFaceWithSimulations
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
 - IDWriteFontFaceReference.CreateFontFaceWithSimulations
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
- IDWriteFontFaceReference.CreateFontFaceWithSimulations
: 
---

# IDWriteFontFaceReference::CreateFontFaceWithSimulations


## -description


Creates a font face with alternate font simulations, for example, to explicitly simulate a bold font face out of a regular variant.


## -parameters




### -param fontFaceSimulationFlags

Type: <b><a href="https://msdn.microsoft.com/0881afec-2fa5-4f17-96a2-68a5293e0bba">DWRITE_FONT_SIMULATIONS</a></b>

Font face simulation flags for algorithmic emboldening and italicization.


### -param fontFace [out]

Type: <b><a href="https://msdn.microsoft.com/1081A005-E4A8-4EE0-AFE0-10BD8D8471DF">IDWriteFontFace3</a>**</b>

Newly created font face object, or nullptr in the case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function can fail with DWRITE_E_REMOTEFONT if the font is not local.




## -see-also




<a href="https://msdn.microsoft.com/04242508-7439-43B6-B3E7-07617B782038">IDWriteFontFaceReference</a>
 

 

