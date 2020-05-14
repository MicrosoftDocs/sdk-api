---
UID: NF:strmif.IVPManager.SetVideoPortIndex
title: IVPManager::SetVideoPortIndex (strmif.h)
description: The SetVideoPortIndex method instructs the Video Port Manager (VPM) to connect to the specified video port.
helpviewer_keywords: ["IVPManager interface [DirectShow]","SetVideoPortIndex method","IVPManager.SetVideoPortIndex","IVPManager::SetVideoPortIndex","IVPManagerSetVideoPortIndex","SetVideoPortIndex","SetVideoPortIndex method [DirectShow]","SetVideoPortIndex method [DirectShow]","IVPManager interface","dshow.ivpmanager_setvideoportindex","strmif/IVPManager::SetVideoPortIndex"]
old-location: dshow\ivpmanager_setvideoportindex.htm
tech.root: DirectShow
ms.assetid: a75332c9-ce3f-4122-ac6c-45478bb5f82c
ms.date: 12/05/2018
ms.keywords: IVPManager interface [DirectShow],SetVideoPortIndex method, IVPManager.SetVideoPortIndex, IVPManager::SetVideoPortIndex, IVPManagerSetVideoPortIndex, SetVideoPortIndex, SetVideoPortIndex method [DirectShow], SetVideoPortIndex method [DirectShow],IVPManager interface, dshow.ivpmanager_setvideoportindex, strmif/IVPManager::SetVideoPortIndex
f1_keywords:
- strmif/IVPManager.SetVideoPortIndex
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVPManager.SetVideoPortIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVPManager::SetVideoPortIndex


## -description



The <code>SetVideoPortIndex</code> method instructs the Video Port Manager (VPM) to connect to the specified video port.




## -parameters




### -param dwVideoPortIndex [in]

Double word containing the video port index.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Use this method on a multi-monitor system to specify to the Video Port Manager which video port index is being used.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivpmanager">IVPManager Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/nf-strmif-ivpmanager-getvideoportindex">IVPManager::GetVideoPortIndex</a>
 

 

