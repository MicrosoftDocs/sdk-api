---
UID: NF:dwrite.IDWriteTextLayout.GetInlineObject
title: IDWriteTextLayout::GetInlineObject
author: windows-sdk-content
description: Gets the inline object at the specified position.
old-location: directwrite\IDWriteTextLayout_GetInlineObject.htm
tech.root: DirectWrite
ms.assetid: 0d86f2a4-d046-4d27-b128-40f2a3dd359a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetInlineObject, GetInlineObject method [Direct Write], GetInlineObject method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetInlineObject method, IDWriteTextLayout.GetInlineObject, IDWriteTextLayout::GetInlineObject, directwrite.IDWriteTextLayout_GetInlineObject, dwrite/IDWriteTextLayout::GetInlineObject
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
 - IDWriteTextLayout.GetInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetInlineObject


## -description


 Gets the inline object at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The specified text position.


### -param inlineObject [out]

Type: <b><a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>**</b>

Contains the application-defined inline object.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the inline object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

