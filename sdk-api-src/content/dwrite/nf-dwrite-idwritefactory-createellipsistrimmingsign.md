---
UID: NF:dwrite.IDWriteFactory.CreateEllipsisTrimmingSign
title: IDWriteFactory::CreateEllipsisTrimmingSign
author: windows-sdk-content
description: Creates an inline object for trimming, using an ellipsis as the omission sign.
old-location: directwrite\IDWriteFactory_CreateEllipsisTrimmingSign.htm
tech.root: DirectWrite
ms.assetid: b416d9f7-d2ce-477c-bf03-b20da2a55bb6
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateEllipsisTrimmingSign, CreateEllipsisTrimmingSign method [Direct Write], CreateEllipsisTrimmingSign method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateEllipsisTrimmingSign method, IDWriteFactory.CreateEllipsisTrimmingSign, IDWriteFactory::CreateEllipsisTrimmingSign, directwrite.IDWriteFactory_CreateEllipsisTrimmingSign, dwrite/IDWriteFactory::CreateEllipsisTrimmingSign
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
 - IDWriteFactory.CreateEllipsisTrimmingSign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateEllipsisTrimmingSign


## -description


 Creates an inline object for trimming, using an ellipsis as the omission sign.
     


## -parameters




### -param textFormat

Type: <b><a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>*</b>

A text format object, created with <a href="https://msdn.microsoft.com/d6e7caba-5cba-4b6e-b146-10aa6d21cac1">CreateTextFormat</a>, used for text layout.


### -param trimmingSign [out]

Type: <b><a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>**</b>

When this method returns, contains an address of a pointer to the omission (that is, ellipsis trimming) sign created by this method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ellipsis will be created using the current settings of the format, including base font, style, and any effects.
     Alternate omission signs can be created by the application by implementing <a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

