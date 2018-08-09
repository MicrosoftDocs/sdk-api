---
UID: NF:vidcap.ICameraControl.get_Focus
title: ICameraControl::get_Focus
author: windows-sdk-content
description: The get_Focus method returns the distance that is optimally in focus.
old-location: dshow\icameracontrol_get_focus.htm
old-project: DirectShow
ms.assetid: 59ab6306-539f-4be4-8e69-348eab6220ea
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: ICameraControl interface [DirectShow],get_Focus method, ICameraControl.get_Focus, ICameraControl::get_Focus, ICameraControlget_Focus, dshow.icameracontrol_get_focus, get_Focus, get_Focus method [DirectShow], get_Focus method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Focus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.get_Focus
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_Focus


## -description


The <code>get_Focus</code> method returns the distance that is optimally in focus.


## -parameters




### -param pValue [out]

Receives the distance that is in focus, in millimeters.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

