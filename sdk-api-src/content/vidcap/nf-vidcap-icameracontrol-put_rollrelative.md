---
UID: NF:vidcap.ICameraControl.put_RollRelative
title: ICameraControl::put_RollRelative method
author: windows-driver-content
description: The put_RollRelative method sets the camera's relative roll. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_put_rollrelative.htm
old-project: DirectShow
ms.assetid: b0dbfd1c-493f-4f35-88ab-cd3868a56370
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], put_RollRelative method, ICameraControl::put_RollRelative, ICameraControlput_RollRelative, dshow.icameracontrol_put_rollrelative, put_RollRelative method [DirectShow], put_RollRelative method [DirectShow], ICameraControl interface, put_RollRelative,ICameraControl.put_RollRelative, vidcap/ICameraControl::put_RollRelative
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
req.typenames: VIDEOHDR, *PVIDEOHDR, *LPVIDEOHDR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	ICameraControl.put_RollRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::put_RollRelative method


## -description


The <code>put_RollRelative</code> method sets the camera's relative roll. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param Value [in]

Specifies the relative roll. The size of the value represents the desired rotation speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://msdn.microsoft.com/c0208111-8648-4511-99f6-20489a026c91">ICameraControl::getRange_RollRelative</a>.

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
<td>Stop the roll.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start rotating clockwise around the viewing axis.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start rotating counterclockwise around the viewing axis.</td>
</tr>
</table>
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

