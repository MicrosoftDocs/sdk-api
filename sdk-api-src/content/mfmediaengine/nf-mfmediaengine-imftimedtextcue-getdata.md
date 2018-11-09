---
UID: NF:mfmediaengine.IMFTimedTextCue.GetData
title: IMFTimedTextCue::GetData
author: windows-sdk-content
description: Gets the data content of the timed-text cue.
old-location: mf\imftimedtextcue_getdata.htm
tech.root: medfound
ms.assetid: 18884B70-DE34-494E-A029-6DD48AB0BA13
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetData, GetData method [Media Foundation], GetData method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetData method, IMFTimedTextCue.GetData, IMFTimedTextCue::GetData, mf.imftimedtextcue_getdata, mfmediaengine/IMFTimedTextCue::GetData
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
 - IMFTimedTextCue.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextCue::GetData


## -description


Gets the data content of the timed-text cue.


## -parameters




### -param data

TBD




#### - ppData [out]

Type: <b><a href="https://msdn.microsoft.com/C76FAC0F-6C15-4874-BAE6-7315E1C3066E">IMFTimedTextBinary</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/C76FAC0F-6C15-4874-BAE6-7315E1C3066E">IMFTimedTextBinary</a> interface for the data content of the timed-text cue. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

