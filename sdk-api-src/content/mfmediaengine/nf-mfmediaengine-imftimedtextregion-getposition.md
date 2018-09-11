---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetPosition
title: IMFTimedTextRegion::GetPosition
author: windows-sdk-content
description: Gets the position of the region.
old-location: mf\imftimedtextregion_getposition.htm
tech.root: medfound
ms.assetid: 1DEE0689-A428-4121-9ED5-5E4D1376461E
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetPosition, GetPosition method [Media Foundation], GetPosition method [Media Foundation],IMFTimedTextRegion interface, IMFTimedTextRegion interface [Media Foundation],GetPosition method, IMFTimedTextRegion.GetPosition, IMFTimedTextRegion::GetPosition, mf.imftimedtextregion_getposition, mfmediaengine/IMFTimedTextRegion::GetPosition
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
 - IMFTimedTextRegion.GetPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTimedTextRegion::GetPosition


## -description


Gets the position of the region.


## -parameters




### -param pX [out]

Type: <b>double*</b>

A pointer to a variable that receives the X-coordinate of the position.


### -param pY [out]

Type: <b>double*</b>

A pointer to a variable that receives the Y-coordinate of the position.


### -param unitType

TBD




#### - pUnitType [out]

Type: <b><a href="https://msdn.microsoft.com/5F811CEC-9E60-4441-BD22-1C4F4D0B72F8">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/5F811CEC-9E60-4441-BD22-1C4F4D0B72F8">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

