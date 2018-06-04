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

# IMFTimedTextFormattedText::GetSubformatting


## -description


Gets a subformat in the formatted timed-text object.


## -parameters




### -param index




### -param firstChar




### -param charLength




### -param style






#### - nIndex [in]

Type: <b>DWORD</b>

The index of the subformat in the formatted timed-text object.


#### - pcchCharLength [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the length, in characters, of the subformat.




#### - pnFirstChar [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the first character of the subformat.




#### - ppStyle [out]

Type: <b><a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a> interface for the subformat's timed-text style. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/98327CA2-21C4-481F-B979-12C31AA1E7B2">IMFTimedTextFormattedText</a>
 

 

