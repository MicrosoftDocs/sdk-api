---
UID: NF:dwrite.IDWriteTextLayout.GetUnderline
title: IDWriteTextLayout::GetUnderline
author: windows-sdk-content
description: Gets the underline presence of the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetUnderline.htm
tech.root: DirectWrite
ms.assetid: cd34ba6b-748c-44ca-8db6-d4715a057def
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetUnderline, GetUnderline method [Direct Write], GetUnderline method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetUnderline method, IDWriteTextLayout.GetUnderline, IDWriteTextLayout::GetUnderline, directwrite.IDWriteTextLayout_GetUnderline, dwrite/IDWriteTextLayout::GetUnderline
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
 - IDWriteTextLayout.GetUnderline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetUnderline


## -description


 Gets the underline presence of the text at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The current text position.


### -param hasUnderline [out]

Type: <b>BOOL*</b>

A Boolean  flag that indicates whether underline is present at the position indicated by <i>currentPosition</i>.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the underline.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

