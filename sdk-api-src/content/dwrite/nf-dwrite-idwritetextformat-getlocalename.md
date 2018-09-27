---
UID: NF:dwrite.IDWriteTextFormat.GetLocaleName
title: IDWriteTextFormat::GetLocaleName
author: windows-sdk-content
description: Gets a copy of the locale name.
old-location: directwrite\IDWriteTextFormat_GetLocaleName.htm
tech.root: DirectWrite
ms.assetid: 89b35622-0898-4fc5-9871-b75244e4dba6
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetLocaleName, GetLocaleName method [Direct Write], GetLocaleName method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetLocaleName method, IDWriteTextFormat.GetLocaleName, IDWriteTextFormat::GetLocaleName, directwrite.IDWriteTextFormat_GetLocaleName, dwrite/IDWriteTextFormat::GetLocaleName
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
 - IDWriteTextFormat.GetLocaleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat::GetLocaleName


## -description


 Gets a copy of the locale name.


## -parameters




### -param localeName [out]

Type: <b>WCHAR*</b>

Contains a character array that receives the current locale name.


### -param nameSize

Type: <b>UINT32</b>

The size of the character array, in character count, including the terminated <b>NULL</b> character. Use <a href="https://msdn.microsoft.com/197926ad-ff96-48b3-872b-22a683725ef8">GetLocaleNameLength</a> to get the size of the locale name character array.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

