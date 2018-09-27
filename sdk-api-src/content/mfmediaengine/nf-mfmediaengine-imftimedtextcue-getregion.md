---
UID: NF:mfmediaengine.IMFTimedTextCue.GetRegion
title: IMFTimedTextCue::GetRegion
author: windows-sdk-content
description: Gets info about the display region of the timed-text cue.
old-location: mf\imftimedtextcue_getregion.htm
tech.root: medfound
ms.assetid: 8F5CE96E-9714-4F1A-8CB5-87FA24735B9D
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetRegion, GetRegion method [Media Foundation], GetRegion method [Media Foundation],IMFTimedTextCue interface, IMFTimedTextCue interface [Media Foundation],GetRegion method, IMFTimedTextCue.GetRegion, IMFTimedTextCue::GetRegion, mf.imftimedtextcue_getregion, mfmediaengine/IMFTimedTextCue::GetRegion
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
 - IMFTimedTextCue.GetRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextCue::GetRegion


## -description


Gets info about the display region  of the timed-text cue.


## -parameters




### -param region

TBD




#### - ppRegion [out]

Type: <b><a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a> interface for the timed-text region. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/831FA230-D0C4-4115-8447-D882686D80EE">IMFTimedTextCue</a>
 

 

