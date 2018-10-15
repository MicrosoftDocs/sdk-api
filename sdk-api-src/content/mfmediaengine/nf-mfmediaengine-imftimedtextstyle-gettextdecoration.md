---
UID: NF:mfmediaengine.IMFTimedTextStyle.GetTextDecoration
title: IMFTimedTextStyle::GetTextDecoration
author: windows-sdk-content
description: Gets how text is decorated for the timed-text style.
old-location: mf\imftimedtextstyle_gettextdecoration.htm
tech.root: medfound
ms.assetid: 5B987C19-5F59-4B5D-BA40-341FA4B3CD35
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetTextDecoration, GetTextDecoration method [Media Foundation], GetTextDecoration method [Media Foundation],IMFTimedTextStyle interface, IMFTimedTextStyle interface [Media Foundation],GetTextDecoration method, IMFTimedTextStyle.GetTextDecoration, IMFTimedTextStyle::GetTextDecoration, mf.imftimedtextstyle_gettextdecoration, mfmediaengine/IMFTimedTextStyle::GetTextDecoration
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
 - IMFTimedTextStyle.GetTextDecoration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextStyle::GetTextDecoration


## -description


Gets how text is decorated for the timed-text style.


## -parameters




### -param textDecoration

TBD




#### - pdwTextDecoration [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives a combination of <a href="https://msdn.microsoft.com/CA2AFC99-F30F-4AFC-928A-45EA7218B851">MF_TIMED_TEXT_DECORATION</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies how text is decorated.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ED358A36-BEEF-491E-8984-938F71472F26">IMFTimedTextStyle</a>
 

 

