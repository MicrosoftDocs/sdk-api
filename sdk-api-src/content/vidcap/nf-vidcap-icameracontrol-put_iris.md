---
UID: NF:vidcap.ICameraControl.put_Iris
title: ICameraControl::put_Iris
author: windows-sdk-content
description: The put_Iris method sets the camera's aperture setting.
old-location: dshow\icameracontrol_put_iris.htm
tech.root: DirectShow
ms.assetid: b181f556-3d3d-4622-8cc9-57fda50bf9c0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],put_Iris method, ICameraControl.put_Iris, ICameraControl::put_Iris, ICameraControlput_Iris, dshow.icameracontrol_put_iris, put_Iris, put_Iris method [DirectShow], put_Iris method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_Iris
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
 - ICameraControl.put_Iris
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::put_Iris


## -description


The <code>put_Iris</code> method sets the camera's aperture setting.


## -parameters




### -param Value [in]

Specifies the aperture setting, in units of f-stop * 10.


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd318251(v=VS.85).aspx">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

