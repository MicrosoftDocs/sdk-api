---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetRightToLeft
title: IMFTimedTextStyle::GetRightToLeft
author: windows-sdk-content
description: Determines whether the right to left writing mode of the timed-text style is enabled.
old-location: mf\imftimedtextstyle_getrighttoleft.htm
tech.root: medfound
ms.assetid: 6BE5C8A0-F577-4E1D-8DB7-3FFBEF059C18
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetRightToLeft, GetRightToLeft method [Media Foundation], GetRightToLeft method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetRightToLeft method, IMFTimedTextStyle.GetRightToLeft, IMFTimedTextStyle::GetRightToLeft, mf.imftimedtextstyle_getrighttoleft, mfmediaengine/IMFTimedTextStyle::GetRightToLeft
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
 - IMFTimedTextStyle.GetRightToLeft
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextStyle::GetRightToLeft


## -description


Determines whether the right to left writing mode of the timed-text style  is enabled.


## -parameters




### -param rightToLeft

TBD




#### - pfRightToLeft [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether the right to left writing mode is enabled. The variable specifies <b>TRUE</b> if the right to left writing mode is enabled; otherwise, <b>FALSE</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>
 

 

