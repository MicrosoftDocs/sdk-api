---
UID: NN:emptyvc.IEmptyVolumeCache
title: IEmptyVolumeCache (emptyvc.h)
description: Used by the disk cleanup manager to communicate with a disk cleanup handler. Exposes methods that enable the manager to request information from a handler, and notify it of events such as the start of a scan or purge.
helpviewer_keywords: ["IEmptyVolumeCache","IEmptyVolumeCache interface [Legacy Windows Environment Features]","IEmptyVolumeCache interface [Legacy Windows Environment Features]","described","_win32_IEmptyVolumeCache","emptyvc/IEmptyVolumeCache","lwef.iemptyvolumecache","shell.iemptyvolumecache"]
old-location: lwef\iemptyvolumecache.htm
tech.root: lwef
ms.assetid: ba3797c2-f82c-4721-b72d-8552683a10d2
ms.date: 12/05/2018
ms.keywords: IEmptyVolumeCache, IEmptyVolumeCache interface [Legacy Windows Environment Features], IEmptyVolumeCache interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCache, emptyvc/IEmptyVolumeCache, lwef.iemptyvolumecache, shell.iemptyvolumecache
req.header: emptyvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEmptyVolumeCache
 - emptyvc/IEmptyVolumeCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IEmptyVolumeCache
---

# IEmptyVolumeCache interface


## -description

Used by the disk cleanup manager to communicate with a disk cleanup handler. Exposes methods that enable the manager to request information from a handler, and notify it of events such as the start of a scan or purge.

## -inheritance

The <b>IEmptyVolumeCache</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEmptyVolumeCache</b> also has these types of members:

## -remarks

This interface must be implemented by disk cleanup handlers running on Windows 98. Handlers running on Windows 2000 should also expose <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache2">IEmptyVolumeCache2</a>.

## -see-also

<a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecachecallback">IEmptyVolumeCacheCallBack</a>
