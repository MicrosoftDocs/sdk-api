---
UID: NN:emptyvc.IEmptyVolumeCacheCallBack
title: IEmptyVolumeCacheCallBack (emptyvc.h)
description: Exposes methods that are used by a disk cleanup handler to communicate with the disk cleanup manager.
helpviewer_keywords: ["IEmptyVolumeCacheCallBack","IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features]","IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features]","described","_win32_IEmptyVolumeCacheCallBack","emptyvc/IEmptyVolumeCacheCallBack","lwef.iemptyvolumecachecallback","shell.iemptyvolumecachecallback"]
old-location: lwef\iemptyvolumecachecallback.htm
tech.root: lwef
ms.assetid: d6775458-3b39-4ee8-90f9-d8a749bd1800
ms.date: 12/05/2018
ms.keywords: IEmptyVolumeCacheCallBack, IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features], IEmptyVolumeCacheCallBack interface [Legacy Windows Environment Features],described, _win32_IEmptyVolumeCacheCallBack, emptyvc/IEmptyVolumeCacheCallBack, lwef.iemptyvolumecachecallback, shell.iemptyvolumecachecallback
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
 - IEmptyVolumeCacheCallBack
 - emptyvc/IEmptyVolumeCacheCallBack
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
 - IEmptyVolumeCacheCallBack
---

# IEmptyVolumeCacheCallBack interface


## -description

Exposes methods that are used by a disk cleanup handler to communicate with the disk cleanup manager.

## -inheritance

The <b>IEmptyVolumeCacheCallBack</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEmptyVolumeCacheCallBack</b> also has these types of members:

## -remarks

A disk cleanup handler uses this interface to report to the disk cleanup manager on the progress either of deleting files or of scanning for deletable files. It also provides a way to query the manager, to find out if the user has canceled the operation. The handler receives a pointer to this interface when the manager calls the <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused">IEmptyVolumeCache::GetSpaceUsed</a> or <a href="/windows/desktop/api/emptyvc/nf-emptyvc-iemptyvolumecache-purge">IEmptyVolumeCache::Purge</a> methods.
