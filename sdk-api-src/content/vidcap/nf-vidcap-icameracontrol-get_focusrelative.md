---
UID: NF:vidcap.ICameraControl.get_FocusRelative
title: ICameraControl::get_FocusRelative
author: windows-sdk-content
description: The get_FocusRelative method returns the relative focus. The relative focus indicates the direction in which the lens group is moving.
old-location: dshow\icameracontrol_get_focusrelative.htm
tech.root: DirectShow
ms.assetid: 21bc1cbe-747b-4846-814f-1aed0ac614d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],get_FocusRelative method, ICameraControl.get_FocusRelative, ICameraControl::get_FocusRelative, ICameraControlget_FocusRelative, dshow.icameracontrol_get_focusrelative, get_FocusRelative, get_FocusRelative method [DirectShow], get_FocusRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_FocusRelative
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
 - ICameraControl.get_FocusRelative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::get_FocusRelative


## -description


The <code>get_FocusRelative</code> method returns the relative focus. The relative focus indicates the direction in which the lens group is moving.


## -parameters




### -param pValue [out]

Receives the relative focus. The size of the value represents the speed at which the focal point changes; a higher value represents a higher speed. To get the range of possible values, call <a href="https://msdn.microsoft.com/en-us/library/Dd376302(v=VS.85).aspx">ICameraControl::getRange_FocusRelative</a>.

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
<td>Focus is moving closer to the object.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Focus is moving farther away from the object.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/en-us/library/Dd318251(v=VS.85).aspx">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd376298(v=VS.85).aspx">ICameraControl Interface</a>
 

 

