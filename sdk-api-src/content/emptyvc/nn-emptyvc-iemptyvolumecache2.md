---
UID: NN:emptyvc.IEmptyVolumeCache2
title: IEmptyVolumeCache2 (emptyvc.h)
description: Extends IEmptyVolumeCache. This interface defines one additional method, InitializeEx, that provides better localization support than IEmptyVolumeCache::Initialize.
helpviewer_keywords: ["IEmptyVolumeCache2","IEmptyVolumeCache2 interface [Legacy Windows Environment Features]","IEmptyVolumeCache2 interface [Legacy Windows Environment Features]","described","_win32_IEmptyVolumeCache2","emptyvc/IEmptyVolumeCache2","lwef.iemptyvolumecache2","shell.iemptyvolumecache2"]
old-location: lwef\iemptyvolumecache2.htm
tech.root: lwef
ms.assetid: a3e941ee-0477-48a8-96bd-c9d74c66ca41
ms.date: 12/05/2018
ms.keywords: IEmptyVolumeCache2, IEmptyVolumeCache2 interface [Legacy Windows Environment Features], IEmptyVolumeCache2 interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCache2, emptyvc/IEmptyVolumeCache2, lwef.iemptyvolumecache2, shell.iemptyvolumecache2
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
 - IEmptyVolumeCache2
 - emptyvc/IEmptyVolumeCache2
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
 - IEmptyVolumeCache2
---

# IEmptyVolumeCache2 interface


## -description

Extends <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>. This interface defines one additional method, <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex">InitializeEx</a>, that provides better localization support than <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-initialize">IEmptyVolumeCache::Initialize</a>.

## -inheritance

The <b>IEmptyVolumeCache2</b> interface inherits from <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>. <b>IEmptyVolumeCache2</b> also has these types of members:

## -remarks

This interface should be exported by disk cleanup handlers running on Windows 2000. Handlers running on Windows 98 must export <a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>.

## -see-also

<a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecache">IEmptyVolumeCache</a>



<a href="/windows/desktop/api/emptyvc/nn-emptyvc-iemptyvolumecachecallback">IEmptyVolumeCacheCallBack</a>
