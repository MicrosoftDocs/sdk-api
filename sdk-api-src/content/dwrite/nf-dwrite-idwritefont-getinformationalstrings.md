---
UID: NF:dwrite.IDWriteFont.GetInformationalStrings
title: IDWriteFont::GetInformationalStrings
author: windows-sdk-content
description: Gets a localized strings collection containing the specified informational strings, indexed by locale name.
old-location: directwrite\IDWriteFont_GetInformationalStrings.htm
old-project: DirectWrite
ms.assetid: a23fec10-4027-45eb-9c29-01df385b24e7
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetInformationalStrings, GetInformationalStrings method [Direct Write], GetInformationalStrings method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetInformationalStrings method, IDWriteFont.GetInformationalStrings, IDWriteFont::GetInformationalStrings, directwrite.IDWriteFont_GetInformationalStrings, dwrite/IDWriteFont::GetInformationalStrings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFont.GetInformationalStrings
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFont::GetInformationalStrings


## -description


 Gets a localized strings collection containing the specified informational strings, indexed by locale name.


## -parameters




### -param informationalStringID

Type: <b><a href="https://msdn.microsoft.com/bbd5ea62-0837-49e4-a1e8-1d55d5d39ee3">DWRITE_INFORMATIONAL_STRING_ID</a></b>

A value that identifies the  informational string to get. For example, <a href="https://msdn.microsoft.com/bbd5ea62-0837-49e4-a1e8-1d55d5d39ee3">DWRITE_INFORMATIONAL_STRING_DESCRIPTION</a> specifies a string that contains a description of the font. 


### -param informationalStrings [out]

Type: <b><a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>**</b>

When this method returns, contains an address of a pointer to the newly created localized strings object.


### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, <b>TRUE</b> if the font contains the specified string ID; otherwise, <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 If the font does not contain the string specified by <i>informationalStringID</i>, the return value is <b>S_OK</b> but 
     <i>informationalStrings</i> receives a <b>NULL</b> pointer and <i>exists</i> receives the value <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/e29e626f-3e63-4c27-934b-64be51dcf3db">IDWriteFont</a>
 

 

