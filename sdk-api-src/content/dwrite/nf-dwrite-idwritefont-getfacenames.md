---
UID: NF:dwrite.IDWriteFont.GetFaceNames
title: IDWriteFont::GetFaceNames (dwrite.h)
author: windows-sdk-content
description: Gets a localized strings collection containing the face names for the font (such as Regular or Bold), indexed by locale name.
old-location: directwrite\IDWriteFont_GetFaceNames.htm
tech.root: DirectWrite
ms.assetid: 6475610a-68f0-4568-9d47-c83515dfa761
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFaceNames, GetFaceNames method [Direct Write], GetFaceNames method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetFaceNames method, IDWriteFont.GetFaceNames, IDWriteFont::GetFaceNames, directwrite.IDWriteFont_GetFaceNames, dwrite/IDWriteFont::GetFaceNames
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
 - IDWriteFont.GetFaceNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFont::GetFaceNames


## -description


 Gets a localized strings collection containing the face names for the font (such as Regular or Bold), indexed by locale name.


## -parameters




### -param names [out]

Type: <b><a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>**</b>

When this method returns, contains an address to a  pointer to the newly created localized strings object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>
 

 

