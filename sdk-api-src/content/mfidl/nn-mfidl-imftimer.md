---
UID: NN:mfidl.IMFTimer
title: IMFTimer (mfidl.h)
description: Provides a timer that invokes a callback at a specified time.
helpviewer_keywords: ["152594df-de3d-4f6f-9277-dba95ab3533a","IMFTimer","IMFTimer interface [Media Foundation]","IMFTimer interface [Media Foundation]","described","mf.imftimer","mfidl/IMFTimer"]
old-location: mf\imftimer.htm
tech.root: mf
ms.assetid: 152594df-de3d-4f6f-9277-dba95ab3533a
ms.date: 12/05/2018
ms.keywords: 152594df-de3d-4f6f-9277-dba95ab3533a, IMFTimer, IMFTimer interface [Media Foundation], IMFTimer interface [Media Foundation],described, mf.imftimer, mfidl/IMFTimer
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTimer
 - mfidl/IMFTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTimer
---

# IMFTimer interface


## -description

Provides a timer that invokes a callback at a specified time.

## -inheritance

The <b>IMFTimer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTimer</b> also has these types of members:

## -remarks

The presentation clock exposes this interface. To get a pointer to the interface, call <b>QueryInterface</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/presentation-clock">Presentation Clock</a>
