---
UID: NF:vidcap.ICameraControl.put_ExposureRelative
title: ICameraControl::put_ExposureRelative
author: windows-sdk-content
description: The put_ExposureRelative method sets the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_put_exposurerelative.htm
tech.root: DirectShow
ms.assetid: 4afc3f7f-bba2-4160-b917-c792467d6305
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ICameraControl interface [DirectShow],put_ExposureRelative method, ICameraControl.put_ExposureRelative, ICameraControl::put_ExposureRelative, ICameraControlput_ExposureRelative, dshow.icameracontrol_put_exposurerelative, put_ExposureRelative, put_ExposureRelative method [DirectShow], put_ExposureRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_ExposureRelative
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
 - ICameraControl.put_ExposureRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vidcap.h
: 
- ICameraControl.put_ExposureRelative
: 
---

# ICameraControl::put_ExposureRelative


## -description


The <code>put_ExposureRelative</code> method sets the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param Value [in]

Specifies the relative exposure. To get the range of possible values, call <a href="https://msdn.microsoft.com/ab46e893-037a-42bb-a3ae-bef943cd6a5e">ICameraControl::getRange_ExposureRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Set the exposure to the default exposure time, which is implementation dependent.</td>
</tr>
<tr>
<td>Postive value</td>
<td>Increment the exposure time by one step.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Decrement the exposure time by one step.</td>
</tr>
</table>
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

