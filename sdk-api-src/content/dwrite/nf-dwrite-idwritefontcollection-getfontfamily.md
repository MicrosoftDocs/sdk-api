---
UID: NF:dwrite.IDWriteFontCollection.GetFontFamily
title: IDWriteFontCollection::GetFontFamily
author: windows-sdk-content
description: Creates a font family object given a zero-based font family index.
old-location: directwrite\IDWriteFontCollection_GetFontFamily.htm
tech.root: DirectWrite
ms.assetid: 470c63cc-b50f-4b62-98c0-f7ce183bfcfd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFontFamily, GetFontFamily method [Direct Write], GetFontFamily method [Direct Write],IDWriteFontCollection interface, IDWriteFontCollection interface [Direct Write],GetFontFamily method, IDWriteFontCollection.GetFontFamily, IDWriteFontCollection::GetFontFamily, directwrite.IDWriteFontCollection_GetFontFamily, dwrite/IDWriteFontCollection::GetFontFamily
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
 - IDWriteFontCollection.GetFontFamily
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteFontCollection.GetFontFamily
: 
---

# IDWriteFontCollection::GetFontFamily


## -description


 Creates a font family object given a zero-based font family index.


## -parameters




### -param index

Type: <b>UINT32</b>

Zero-based index of the font family.


### -param fontFamily [out]

Type: <b><a href="https://msdn.microsoft.com/1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13">IDWriteFontFamily</a>**</b>

When this method returns, contains the address of   a pointer to the newly created font family object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>
 

 

