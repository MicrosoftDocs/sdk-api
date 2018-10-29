---
UID: NF:vidcap.ICameraControl.get_ZoomRelative
title: ICameraControl::get_ZoomRelative
author: windows-sdk-content
description: The get_ZoomRelative method returns the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.
old-location: dshow\icameracontrol_get_zoomrelative.htm
tech.root: DirectShow
ms.assetid: c1926541-d7c7-4a16-bbe7-0d93dec89c67
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ICameraControl interface [DirectShow],get_ZoomRelative method, ICameraControl.get_ZoomRelative, ICameraControl::get_ZoomRelative, ICameraControlget_ZoomRelative, dshow.icameracontrol_get_zoomrelative, get_ZoomRelative, get_ZoomRelative method [DirectShow], get_ZoomRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ZoomRelative
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
 - ICameraControl.get_ZoomRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::get_ZoomRelative


## -description


The <code>get_ZoomRelative</code> method returns the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.


## -parameters




### -param pValue [out]

Receives the relative zoom. The size of the value represents the desired zoom speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://msdn.microsoft.com/ea3460b8-b956-4dc9-bed7-f28714e1df11">ICameraControl::getRange_ZoomRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stopped.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Zoom lens moving in the telephoto direction.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Zoom lens moving in the wide angle direction.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

