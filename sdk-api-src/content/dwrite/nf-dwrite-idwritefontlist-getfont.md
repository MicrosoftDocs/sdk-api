---
UID: NF:dwrite.IDWriteFontList.GetFont
title: IDWriteFontList::GetFont
author: windows-sdk-content
description: Gets a font given its zero-based index.
old-location: directwrite\IDWriteFontList_GetFont.htm
tech.root: DirectWrite
ms.assetid: b2262707-b5d5-4697-9634-72fd2a72000a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetFont, GetFont method [Direct Write], GetFont method [Direct Write],IDWriteFontList interface, IDWriteFontList interface [Direct Write],GetFont method, IDWriteFontList.GetFont, IDWriteFontList::GetFont, directwrite.IDWriteFontList_GetFont, dwrite/IDWriteFontList::GetFont
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
 - IDWriteFontList.GetFont
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontList::GetFont


## -description


 Gets a font given its zero-based index.


## -parameters




### -param index

Type: <b>UINT32</b>

Zero-based index of the font in the font list.


### -param font [out]

Type: <b><a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>**</b>

When this method returns, contains the address of a pointer to the newly created <a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/00c41c5f-4405-45ff-98e5-03858dc3056f">IDWriteFontList</a>
 

 

