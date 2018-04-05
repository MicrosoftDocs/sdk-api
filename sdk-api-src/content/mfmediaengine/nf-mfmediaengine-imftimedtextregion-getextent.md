---
UID: NF:mfmediaengine.IMFTimedTextRegion.GetExtent
title: IMFTimedTextRegion::GetExtent method
author: windows-driver-content
description: Gets the extent of the region.
old-location: mf\imftimedtextregion_getextent.htm
old-project: medfound
ms.assetid: 581D9A8D-FBED-4E67-9E81-77D9C29ADF82
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetExtent method [Media Foundation], GetExtent method [Media Foundation], IMFTimedTextRegion interface, GetExtent,IMFTimedTextRegion.GetExtent, IMFTimedTextRegion, IMFTimedTextRegion interface [Media Foundation], GetExtent method, IMFTimedTextRegion::GetExtent, mf.imftimedtextregion_getextent, mfmediaengine/IMFTimedTextRegion::GetExtent
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
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFTimedTextRegion.GetExtent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTimedTextRegion::GetExtent method


## -description


Gets the extent of the region.


## -parameters




### -param pWidth [out]

Type: <b>double*</b>

A pointer to a variable that receives the width of the region.


### -param pHeight [out]

Type: <b>double*</b>

A pointer to a variable that receives the height of the region.


### -param unitType






#### - pUnitType [out]

Type: <b><a href="https://msdn.microsoft.com/5F811CEC-9E60-4441-BD22-1C4F4D0B72F8">MF_TIMED_TEXT_UNIT_TYPE</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/5F811CEC-9E60-4441-BD22-1C4F4D0B72F8">MF_TIMED_TEXT_UNIT_TYPE</a>-typed value that specifies the units in which the timed-text region is measured.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1A6E068F-2E01-4A72-8BCF-D645B1D21ECF">IMFTimedTextRegion</a>
 

 

