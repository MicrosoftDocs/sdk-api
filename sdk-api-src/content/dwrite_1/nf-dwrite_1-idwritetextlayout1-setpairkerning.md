---
UID: NF:dwrite_1.IDWriteTextLayout1.SetPairKerning
title: IDWriteTextLayout1::SetPairKerning (dwrite_1.h)
author: windows-sdk-content
description: Enables or disables pair-kerning on a given text range.
old-location: directwrite\idwritetextlayout1_setpairkerning.htm
tech.root: DirectWrite
ms.assetid: AE43D7E4-CD2D-4BBD-88C3-B5287FD235AF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout1 interface [Direct Write],SetPairKerning method, IDWriteTextLayout1.SetPairKerning, IDWriteTextLayout1::SetPairKerning, SetPairKerning, SetPairKerning method [Direct Write], SetPairKerning method [Direct Write],IDWriteTextLayout1 interface, directwrite.idwritetextlayout1_setpairkerning, dwrite_1/IDWriteTextLayout1::SetPairKerning
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
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
 - IDWriteTextLayout1.SetPairKerning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout1::SetPairKerning


## -description


Enables or disables pair-kerning on a given text range.


## -parameters




### -param isPairKerningEnabled

Type: <b>BOOL</b>

The flag that indicates whether text is pair-kerned.


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

The text range to which the change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/FF6B3C78-0CC0-4843-9D17-3CF0777EA8BA">IDWriteTextLayout1</a>
 

 

