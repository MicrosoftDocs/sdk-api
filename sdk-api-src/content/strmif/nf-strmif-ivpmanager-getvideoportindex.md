---
UID: NF:strmif.IVPManager.GetVideoPortIndex
title: IVPManager::GetVideoPortIndex
author: windows-sdk-content
description: The GetVideoPortIndex method returns the current video port index being used by the Video Port Manager (VPM).
old-location: dshow\ivpmanager_getvideoportindex.htm
tech.root: DirectShow
ms.assetid: 1e30c2d7-b986-47f5-94c8-53937d1e1501
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetVideoPortIndex, GetVideoPortIndex method [DirectShow], GetVideoPortIndex method [DirectShow],IVPManager interface, IVPManager interface [DirectShow],GetVideoPortIndex method, IVPManager.GetVideoPortIndex, IVPManager::GetVideoPortIndex, IVPManagerGetVideoPortIndex, dshow.ivpmanager_getvideoportindex, strmif/IVPManager::GetVideoPortIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVPManager.GetVideoPortIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9064daa7-5868-49a5-9fd6-9a332ab3b470">IVPManager Interface</a>



<a href="https://msdn.microsoft.com/a75332c9-ce3f-4122-ac6c-45478bb5f82c">SetVideoPortIndex</a>
 

 

