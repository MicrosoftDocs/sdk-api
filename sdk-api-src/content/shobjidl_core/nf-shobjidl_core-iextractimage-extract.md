---
UID: NF:shobjidl_core.IExtractImage.Extract
title: IExtractImage::Extract
author: windows-sdk-content
description: Requests an image from an object, such as an item in a Shell folder.
old-location: shell\IExtractImage_Extract.htm
old-project: shell
ms.assetid: 7c40e2cf-c706-4a4a-819f-a416d6846158
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Extract, Extract method [Windows Shell], Extract method [Windows Shell],IExtractImage interface, IExtractImage interface [Windows Shell],Extract method, IExtractImage.Extract, IExtractImage::Extract, _win32_IExtractImage_Extract, shell.IExtractImage_Extract, shobjidl_core/IExtractImage::Extract
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Shell32.dll
api_name:
 - IExtractImage.Extract
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.70 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IExtractImage::Extract


## -description


Requests an image from an object, such as an item in a Shell folder.


## -parameters




### -param phBmpThumbnail






#### - phBmpImage [out]

Type: <b>HBITMAP*</b>

The buffer to hold the bitmapped image.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -remarks



You must call <a href="https://msdn.microsoft.com/f1113429-ea89-4650-b345-db9e275232e6">IExtractImage::GetLocation</a> prior to calling <b>Extract</b>.



