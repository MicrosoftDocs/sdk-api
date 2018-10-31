---
UID: NF:strmif.IAMCameraControl.GetRange
title: IAMCameraControl::GetRange
author: windows-sdk-content
description: The GetRange method gets the range and default value of a specified camera property.
old-location: dshow\iamcameracontrol_getrange.htm
tech.root: DirectShow
ms.assetid: f09090ea-d916-47cd-8621-e8c2bb46aeca
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetRange, GetRange method [DirectShow], GetRange method [DirectShow],IAMCameraControl interface, IAMCameraControl interface [DirectShow],GetRange method, IAMCameraControl.GetRange, IAMCameraControl::GetRange, IAMCameraControlGetRange, dshow.iamcameracontrol_getrange, strmif/IAMCameraControl::GetRange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMCameraControl.GetRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMCameraControl::GetRange


## -description



The <b>GetRange</b> method gets the range and default value of a specified camera property.




## -parameters




### -param Property

TBD


### -param pMin [out]

Receives the minimum value of the property.
          


### -param pMax [out]

Receives the maximum value of the property.
          


### -param pSteppingDelta [out]

Receives the step size for the property. The step size is the smallest increment by which the property can change.
          


### -param pDefault [out]

Receives the default value of the property.
          


### -param pCapsFlags [out]

Receives a member of the <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a> enumeration, indicating whether the property is controlled automatically or manually.
          


#### - property [in]

Specifies the property to query, as a value from the <a href="https://msdn.microsoft.com/eebf2246-960f-48ea-86b7-7542e69f2e3e">CameraControlProperty</a> enumeration.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/22bc35f1-76d4-4881-91d1-72f05c24561d">IAMCameraControl Interface</a>
 

 

