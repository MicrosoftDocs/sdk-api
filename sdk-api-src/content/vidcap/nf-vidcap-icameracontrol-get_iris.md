---
UID: NF:vidcap.ICameraControl.get_Iris
title: ICameraControl::get_Iris
author: windows-sdk-content
description: The get_Iris method returns the camera's aperture setting.
old-location: dshow\icameracontrol_get_iris.htm
old-project: DirectShow
ms.assetid: 710a29f1-f5ab-42cf-b912-dd9b4546757e
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: ICameraControl interface [DirectShow],get_Iris method, ICameraControl.get_Iris, ICameraControl::get_Iris, ICameraControlget_Iris, dshow.icameracontrol_get_iris, get_Iris, get_Iris method [DirectShow], get_Iris method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Iris
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.redist: 
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
 - ICameraControl.get_Iris
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_Iris


## -description


The <code>get_Iris</code> method returns the camera's aperture setting.


## -parameters




### -param pValue [out]

Receives the aperture setting, in units of f-stop * 10.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

