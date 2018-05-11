---
UID: NF:vidcap.ICameraControl.get_ExposureRelative
title: ICameraControl::get_ExposureRelative
author: windows-driver-content
description: The get_ExposureRelative method returns the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_get_exposurerelative.htm
old-project: DirectShow
ms.assetid: d63cf869-ccb6-45cb-85ba-a1e41faa8086
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ICameraControl interface [DirectShow],get_ExposureRelative method, ICameraControl.get_ExposureRelative, ICameraControl::get_ExposureRelative, ICameraControlget_ExposureRelative, dshow.icameracontrol_get_exposurerelative, get_ExposureRelative, get_ExposureRelative method [DirectShow], get_ExposureRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ExposureRelative
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
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICameraControl.get_ExposureRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_ExposureRelative


## -description


The <code>get_ExposureRelative</code> method returns the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pValue [out]

Receives the relative exposure. To get the range of possible values, call <a href="https://msdn.microsoft.com/ab46e893-037a-42bb-a3ae-bef943cd6a5e">ICameraControl::getRange_ExposureRelative</a>.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Default exposure time.</td>
</tr>
<tr>
<td>Postive value</td>
<td>Incremented by one step.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Decremented by one step.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

