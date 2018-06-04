---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFTimedTextStyle::GetTextAlignment


## -description


Gets the text alignment of the timed-text style.


## -parameters




### -param textAlign






#### - pTextAlign [out]

Type: <b><a href="https://msdn.microsoft.com/F94DF6A5-1FF7-48C2-834F-50C90B2D9C33">MF_TIMED_TEXT_ALIGNMENT</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/F94DF6A5-1FF7-48C2-834F-50C90B2D9C33">MF_TIMED_TEXT_ALIGNMENT</a>-typed value that specifies the text alignment.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>
 

 

