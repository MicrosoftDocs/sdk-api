---
UID: NF:vidcap.ICameraControl.put_FocusRelative
title: ICameraControl::put_FocusRelative method
author: windows-driver-content
description: The put_FocusRelative method sets the relative focus. The relative focus indicates the direction in which the lens group is moving.
old-location: dshow\icameracontrol_put_focusrelative.htm
old-project: DirectShow
ms.assetid: d40edc5d-8fa2-4e3a-8aab-c51da0ac8036
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ICameraControl, ICameraControl interface [DirectShow], put_FocusRelative method, ICameraControl::put_FocusRelative, ICameraControlput_FocusRelative, dshow.icameracontrol_put_focusrelative, put_FocusRelative method [DirectShow], put_FocusRelative method [DirectShow], ICameraControl interface, put_FocusRelative,ICameraControl.put_FocusRelative, vidcap/ICameraControl::put_FocusRelative
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
-	ICameraControl.put_FocusRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::put_FocusRelative method


## -description


The <code>put_FocusRelative</code> method sets the relative focus. The relative focus indicates the direction in which the lens group is moving.


## -parameters




### -param Value [in]

Specifies the relative focus. The size of the value represents the speed at which the focal point changes; a higher value represents a higher speed. To get the possible range of values, call <a href="https://msdn.microsoft.com/c5038a59-bdc4-4034-afd1-256003687187">ICameraControl::getRange_FocusRelative</a>.

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
<td>Stop focus motion.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start moving the focus closer to the object.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start moving the focus farther away from the object.</td>
</tr>
</table>
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

