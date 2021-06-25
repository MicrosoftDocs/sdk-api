---
UID: NF:presentation.IIndependentFlipFramePresentStatistics.GetPresentDuration
tech.root: composition_presentation
title: IIndependentFlipFramePresentStatistics::GetPresentDuration
ms.date: 06/08/2021
targetos: Windows
description: Gets the actual amount of time the present was displayed.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: presentation.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - presentation.h
api_name:
 - IIndependentFlipFramePresentStatistics::GetPresentDuration
f1_keywords:
 - IIndependentFlipFramePresentStatistics::GetPresentDuration
 - presentation/IIndependentFlipFramePresentStatistics::GetPresentDuration
dev_langs:
 - c++
---

## -description

Gets the actual amount of time the present was displayed.

## -returns

TYPE: **[SystemInterruptTime](ns-presentationtypes-systeminterrupttime.md)**

The actual amount of time the present was displayed.

## -remarks

The actual present duration may be different from the preferred present duration requested by the application if the system decided not to honor the preferred duration. This usually happens either because it was not supported by the driver, or other content on screen influenced the system to go with another duration.

## -see-also

