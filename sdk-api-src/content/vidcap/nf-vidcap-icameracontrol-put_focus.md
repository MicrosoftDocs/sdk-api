---
UID: NF:vidcap.ICameraControl.put_Focus
title: ICameraControl::put_Focus
author: windows-sdk-content
description: The put_Focus method sets the distance that is optimally in focus.
old-location: dshow\icameracontrol_put_focus.htm
tech.root: DirectShow
ms.assetid: c896bf2b-33b6-4e7c-bf84-b7dd8f57a4d4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ICameraControl interface [DirectShow],put_Focus method, ICameraControl.put_Focus, ICameraControl::put_Focus, ICameraControlput_Focus, dshow.icameracontrol_put_focus, put_Focus, put_Focus method [DirectShow], put_Focus method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Focus
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICameraControl.put_Focus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::put_Focus


## -description


The <code>put_Focus</code> method sets the distance that is optimally in focus.


## -parameters




### -param Value [in]

Specifies the focus distance, in millimeters.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

