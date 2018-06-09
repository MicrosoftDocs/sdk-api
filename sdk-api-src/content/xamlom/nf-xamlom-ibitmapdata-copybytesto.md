---
UID: NF:xamlom.IBitmapData.CopyBytesTo
title: IBitmapData::CopyBytesTo
author: windows-sdk-content
description: Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (pvBytes), and returns the number of bytes copied.
old-location: xaml_diagnostics\ibitmapdata_copybytesto.htm
old-project: xaml_diagnostics
ms.assetid: 8E8CB014-D394-4457-8AC7-773A87EE2643
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CopyBytesTo, CopyBytesTo method, CopyBytesTo method,IBitmapData interface, IBitmapData interface,CopyBytesTo method, IBitmapData.CopyBytesTo, IBitmapData::CopyBytesTo, xaml_diagnostics.ibitmapdata_copybytesto, xamlom/IBitmapData::CopyBytesTo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VisualMutationType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IBitmapData.CopyBytesTo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IBitmapData::CopyBytesTo


## -description


Copies up to the specified maximum number of bytes from the given offset in the bitmap data into the caller’s buffer (<i>pvBytes</i>), and returns the number of bytes copied.


## -parameters




### -param sourceOffsetInBytes [in]

The place in the bitmap data to start copying from, in bytes.


### -param maxBytesToCopy [in]

The maximum number of bytes to copy.


### -param pvBytes [out]

The buffer into which the bytes are copied.


### -param numberOfBytesCopied [out]

The number of bytes copied.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>
 

 

