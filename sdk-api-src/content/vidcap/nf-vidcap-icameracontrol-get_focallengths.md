---
UID: NF:vidcap.ICameraControl.get_FocalLengths
title: ICameraControl::get_FocalLengths (vidcap.h)
author: windows-sdk-content
description: The get_FocalLengths method returns the focal lengths of the camera lenses.
old-location: dshow\icameracontrol_get_focallengths.htm
tech.root: DirectShow
ms.assetid: de566705-1f4b-4ffa-932d-a52521e6963b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_FocalLengths method, ICameraControl.get_FocalLengths, ICameraControl::get_FocalLengths, ICameraControlget_FocalLengths, dshow.icameracontrol_get_focallengths, get_FocalLengths, get_FocalLengths method [DirectShow], get_FocalLengths method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_FocalLengths
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
 - ICameraControl.get_FocalLengths
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::get_FocalLengths


## -description


The <code>get_FocalLengths</code> method returns the focal lengths of the camera lenses.


## -parameters




### -param plOcularFocalLength [out]

Receives the ocular focal length.


### -param plObjectiveFocalLengthMin [out]

Receives the minimum objective focal length.


### -param plObjectiveFocalLengthMax [out]

Receives the maximum objective focal length.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



In a two-lens camera, the objective lens is closer to the subject, and the ocular lens is closer to the camera. The ocular focal length is fixed. If the camera has an optical zoom, the objective focal length can vary within a fixed range. Magnification is calculated as the ratio of objective/ocular focal length. Because the magnification is expressed as a ratio, it has no units. Therefore, the units for the focal length are not defined by this interface.

If the camera supports optical zooming, the current zoom level is expressed as integer values between a range <i>Zmin</i> and <i>Zmax</i>. The objective focal length can then be calculated as follows:


```cpp

Lcur = ( ( (Zcur - Zmin) * (Lmax - Lmin) ) / (Zmax - Zmin) ) + Lmin

```


where:

<ul>
<li>
            Lcur = Current objective focal length.</li>
<li>
            Lmin, Lmax = Minimum and maximum objective focal length.</li>
<li>
            Zcur = Current zoom setting. See <a href="https://msdn.microsoft.com/en-us/library/Dd376330(v=VS.85).aspx">ICameraControl::get_Zoom</a>.</li>
<li>
            Zmin, Zmax = Minimum and maximum zoom setting. See <a href="https://msdn.microsoft.com/en-us/library/Dd376311(v=VS.85).aspx">ICameraControl::getRange_Zoom</a>.</li>
</ul>
From 


```
Lcur
```

, you can calculate the magnification.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

