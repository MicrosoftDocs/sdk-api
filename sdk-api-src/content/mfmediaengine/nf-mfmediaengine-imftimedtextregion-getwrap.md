---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetWrap
title: IMFTimedTextRegion::GetWrap
author: windows-sdk-content
description: Determines whether the word wrap feature is enabled in the region.
old-location: mf\imftimedtextregion_getwrap.htm
old-project: medfound
ms.assetid: 634B686C-A083-4F11-9330-4BD22D93A066
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetWrap, GetWrap method [Media Foundation], GetWrap method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetWrap method, IMFTimedTextRegion.GetWrap, IMFTimedTextRegion::GetWrap, mf.imftimedtextregion_getwrap, mfmediaengine/IMFTimedTextRegion::GetWrap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFTimedTextRegion.GetWrap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextRegion::GetWrap


## -description


Determines whether the word wrap feature is enabled in the region.


## -parameters




### -param wrap






#### - pfWrap [out]

Type: <b>BOOL*</b>

A pointer to a variable that receives a value that specifies whether the word wrap feature is enabled in the region. The variable specifies <b>TRUE</b> if word wrap is enabled; otherwise, <b>FALSE</b>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

