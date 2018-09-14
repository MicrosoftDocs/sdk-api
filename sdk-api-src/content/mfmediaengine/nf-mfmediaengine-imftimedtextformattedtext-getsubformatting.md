---
UID: NF:mfmediaengine.IMFTimedTextFormattedText.GetSubformatting
title: IMFTimedTextFormattedText::GetSubformatting
author: windows-sdk-content
description: Gets a subformat in the formatted timed-text object.
old-location: mf\imftimedtextformattedtext_getsubformatting.htm
tech.root: medfound
ms.assetid: EC6F41A4-BB07-419B-BE03-8D82709D9A24
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetSubformatting, GetSubformatting method [Media Foundation], GetSubformatting method [Media Foundation],IMFTimedTextFormattedText interface, IMFTimedTextFormattedText interface [Media Foundation],GetSubformatting method, IMFTimedTextFormattedText.GetSubformatting, IMFTimedTextFormattedText::GetSubformatting, mf.imftimedtextformattedtext_getsubformatting, mfmediaengine/IMFTimedTextFormattedText::GetSubformatting
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextFormattedText.GetSubformatting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextFormattedText::GetSubformatting


## -description


Gets a subformat in the formatted timed-text object.


## -parameters




### -param index

TBD


### -param firstChar

TBD


### -param charLength

TBD


### -param style

TBD




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
 

 

