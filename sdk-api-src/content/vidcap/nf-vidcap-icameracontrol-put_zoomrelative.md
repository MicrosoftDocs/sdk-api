---
UID: NF:vidcap.ICameraControl.put_ZoomRelative
title: ICameraControl::put_ZoomRelative method
author: windows-driver-content
description: The put_ZoomRelative method sets the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.
old-location: dshow\icameracontrol_put_zoomrelative.htm
old-project: DirectShow
ms.assetid: 815f92c3-bfab-47d5-86dd-f9b2321d20eb
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], put_ZoomRelative method, ICameraControl::put_ZoomRelative, ICameraControlput_ZoomRelative, dshow.icameracontrol_put_zoomrelative, put_ZoomRelative method [DirectShow], put_ZoomRelative method [DirectShow], ICameraControl interface, put_ZoomRelative,ICameraControl.put_ZoomRelative, vidcap/ICameraControl::put_ZoomRelative
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
-	ICameraControl.put_ZoomRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::put_ZoomRelative method


## -description


The <code>put_ZoomRelative</code> method sets the camera's relative zoom. The relative zoom indicates the direction in which the lens is moving.


## -parameters




### -param Value [in]

Specifies the relative zoom. The size of the value represents the desired zoom speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://msdn.microsoft.com/ea3460b8-b956-4dc9-bed7-f28714e1df11">ICameraControl::getRange_ZoomRelative</a>.

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
<td>Stop zoom lens motion.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start moving the zoom lens in the telephoto direction (initiate zoom-in).</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start moving the zoom lens in the wide angle direction (initiate zoom-out).</td>
</tr>
</table>
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

