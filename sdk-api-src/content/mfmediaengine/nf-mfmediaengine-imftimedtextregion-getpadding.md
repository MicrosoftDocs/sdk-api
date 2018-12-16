---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetPadding
title: IMFTimedTextRegion::GetPadding
author: windows-sdk-content
description: Gets the padding that surrounds the region.
old-location: mf\imftimedtextregion_getpadding.htm
tech.root: medfound
ms.assetid: B97ECFD8-2E96-425F-B29E-49E7D53BBFCB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPadding, GetPadding method [Media Foundation], GetPadding method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetPadding method, IMFTimedTextRegion.GetPadding, IMFTimedTextRegion::GetPadding, mf.imftimedtextregion_getpadding, mfmediaengine/IMFTimedTextRegion::GetPadding
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
 - IMFTimedTextRegion.GetPadding
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextRegion::GetPadding


## -description


Gets the padding that surrounds the region.


## -parameters




### -param before [out]

Type: <b>double*</b>

A pointer to a variable that receives the padding before the start of the region.


### -param start [out]

Type: <b>double*</b>

A pointer to a variable that receives the start of the region.


### -param after [out]

Type: <b>double*</b>

A pointer to a variable that receives the padding after the end of the region.


### -param end [out]

Type: <b>double*</b>

A pointer to a variable that receives the end of the region.


### -param unitType [out]

Type: <b><a href="https://msdn.microsoft.com/5F811CEC-9E60-4441-BD22-1C4F4D0B72F8">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/5F811CEC-9E60-4441-BD22-1C4F4D0B72F8">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

