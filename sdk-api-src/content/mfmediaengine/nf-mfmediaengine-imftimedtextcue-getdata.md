---
UID: NF:mfmediaengine.IMFTimedTextCue.GetData
title: IMFTimedTextCue::GetData (mfmediaengine.h)
author: windows-sdk-content
description: Gets the data content of the timed-text cue.
old-location: mf\imftimedtextcue_getdata.htm
tech.root: medfound
ms.assetid: 18884B70-DE34-494E-A029-6DD48AB0BA13
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Media Foundation], GetData method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetData method, IMFTimedTextCue.GetData, IMFTimedTextCue::GetData, mf.imftimedtextcue_getdata, mfmediaengine/IMFTimedTextCue::GetData
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFTimedTextCue.GetData"
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
 - IMFTimedTextCue.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTimedTextCue::GetData


## -description


Gets the data content of the timed-text cue.


## -parameters




### -param data [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary">IMFTimedTextBinary</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary">IMFTimedTextBinary</a> interface for the data content of the timed-text cue. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue">IMFTimedTextCue</a>
 

 

