---
UID: NF:strmif.IVPManager.GetVideoPortIndex
title: IVPManager::GetVideoPortIndex (strmif.h)
description: The GetVideoPortIndex method returns the current video port index being used by the Video Port Manager (VPM).
helpviewer_keywords: ["GetVideoPortIndex","GetVideoPortIndex method [DirectShow]","GetVideoPortIndex method [DirectShow]","IVPManager interface","IVPManager interface [DirectShow]","GetVideoPortIndex method","IVPManager.GetVideoPortIndex","IVPManager::GetVideoPortIndex","IVPManagerGetVideoPortIndex","dshow.ivpmanager_getvideoportindex","strmif/IVPManager::GetVideoPortIndex"]
old-location: dshow\ivpmanager_getvideoportindex.htm
tech.root: DirectShow
ms.assetid: 1e30c2d7-b986-47f5-94c8-53937d1e1501
ms.date: 12/05/2018
ms.keywords: GetVideoPortIndex, GetVideoPortIndex method [DirectShow], GetVideoPortIndex method [DirectShow],IVPManager interface, IVPManager interface [DirectShow],GetVideoPortIndex method, IVPManager.GetVideoPortIndex, IVPManager::GetVideoPortIndex, IVPManagerGetVideoPortIndex, dshow.ivpmanager_getvideoportindex, strmif/IVPManager::GetVideoPortIndex
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPManager::GetVideoPortIndex
 - strmif/IVPManager::GetVideoPortIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVPManager.GetVideoPortIndex
---

# IVPManager::GetVideoPortIndex


## -description

The <code>GetVideoPortIndex</code> method returns the current video port index being used by the Video Port Manager (VPM).

## -parameters

### -param pdwVideoPortIndex [out]

Pointer to a double word containing the index of the video port that the VPM is currently connected to.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns the current video port index being used by the Video Port Manager (VPM).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivpmanager">IVPManager Interface</a>



[SetVideoPortIndex](/windows/desktop/api/strmif/nf-strmif-ivpmanager-setvideoportindex)