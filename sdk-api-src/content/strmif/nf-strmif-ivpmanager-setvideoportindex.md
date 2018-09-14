---
UID: NF:strmif.IVPManager.SetVideoPortIndex
title: IVPManager::SetVideoPortIndex
author: windows-sdk-content
description: The SetVideoPortIndex method instructs the Video Port Manager (VPM) to connect to the specified video port.
old-location: dshow\ivpmanager_setvideoportindex.htm
tech.root: DirectShow
ms.assetid: a75332c9-ce3f-4122-ac6c-45478bb5f82c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IVPManager interface [DirectShow],SetVideoPortIndex method, IVPManager.SetVideoPortIndex, IVPManager::SetVideoPortIndex, IVPManagerSetVideoPortIndex, SetVideoPortIndex, SetVideoPortIndex method [DirectShow], SetVideoPortIndex method [DirectShow],IVPManager interface, dshow.ivpmanager_setvideoportindex, strmif/IVPManager::SetVideoPortIndex
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
 - IVPManager.SetVideoPortIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9064daa7-5868-49a5-9fd6-9a332ab3b470">IVPManager Interface</a>



<a href="https://msdn.microsoft.com/1e30c2d7-b986-47f5-94c8-53937d1e1501">IVPManager::GetVideoPortIndex</a>
 

 

