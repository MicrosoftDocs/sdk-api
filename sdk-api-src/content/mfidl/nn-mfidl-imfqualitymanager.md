---
UID: NN:mfidl.IMFQualityManager
title: IMFQualityManager (mfidl.h)
description: Adjusts playback quality. This interface is exposed by the quality manager.
helpviewer_keywords: ["66781a1f-7469-4222-9e99-6b1415830f4c","IMFQualityManager","IMFQualityManager interface [Media Foundation]","IMFQualityManager interface [Media Foundation]","described","mf.imfqualitymanager","mfidl/IMFQualityManager"]
old-location: mf\imfqualitymanager.htm
tech.root: mf
ms.assetid: 66781a1f-7469-4222-9e99-6b1415830f4c
ms.date: 12/05/2018
ms.keywords: 66781a1f-7469-4222-9e99-6b1415830f4c, IMFQualityManager, IMFQualityManager interface [Media Foundation], IMFQualityManager interface [Media Foundation],described, mf.imfqualitymanager, mfidl/IMFQualityManager
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
 - IMFQualityManager
 - mfidl/IMFQualityManager
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
 - IMFQualityManager
---

# IMFQualityManager interface


## -description

Adjusts playback quality. This interface is exposed by the quality manager.

## -inheritance

The <b>IMFQualityManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFQualityManager</b> also has these types of members:

## -remarks

Media Foundation provides a default quality manager that is tuned for playback. Applications can provide a custom quality manager to the Media Session by setting the <a href="/windows/desktop/medfound/mf-session-quality-manager-attribute">MF_SESSION_QUALITY_MANAGER</a> attribute when creating the Media Session.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
