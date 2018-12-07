---
UID: NF:dwrite.IDWriteTextLayout.SetInlineObject
title: IDWriteTextLayout::SetInlineObject
author: windows-sdk-content
description: Sets the inline object.
old-location: directwrite\IDWriteTextLayout_SetInlineObject.htm
tech.root: DirectWrite
ms.assetid: 19fc9dd8-d732-4078-9db3-bad18681c7ea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetInlineObject method, IDWriteTextLayout.SetInlineObject, IDWriteTextLayout::SetInlineObject, SetInlineObject, SetInlineObject method [Direct Write], SetInlineObject method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetInlineObject, dwrite/IDWriteTextLayout::SetInlineObject
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
 - IDWriteTextLayout.SetInlineObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::SetInlineObject


## -description


 Sets the inline object.


## -parameters




### -param inlineObject

Type: <b><a href="https://msdn.microsoft.com/cf915458-acbc-4a37-be5c-b1337153f386">IDWriteInlineObject</a>*</b>

An application-defined inline object. 


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The application may call this function to specify the set of properties describing an application-defined inline object for specific range.

 This inline object applies to the specified range and will be passed back
     to the application by way of the <a href="https://msdn.microsoft.com/ea1c4cd0-d9b5-46af-b53e-a2d8fc442acf">DrawInlineObject</a> callback when the range is drawn.
     Any text in that range will be suppressed.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

