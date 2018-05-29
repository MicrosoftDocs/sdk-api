---
UID: NF:vidcap.ICameraControl.get_PanRelative
title: ICameraControl::get_PanRelative
author: windows-sdk-content
description: The get_PanRelative method returns the camera's relative pan. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.
old-location: dshow\icameracontrol_get_panrelative.htm
old-project: DirectShow
ms.assetid: a7237e0a-82b3-4e2a-a6c7-97fbb03b5917
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: ICameraControl interface [DirectShow],get_PanRelative method, ICameraControl.get_PanRelative, ICameraControl::get_PanRelative, ICameraControlget_PanRelative, dshow.icameracontrol_get_panrelative, get_PanRelative, get_PanRelative method [DirectShow], get_PanRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PanRelative
ms.prod: windows
ms.technology: windows-sdk
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
-	ICameraControl.get_PanRelative
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_PanRelative


## -description


The <code>get_PanRelative</code> method returns the camera's relative pan. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pValue [out]

Receives the relative pan. The size of the value represents the desired pan speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://msdn.microsoft.com/31affca6-e9e9-4715-aea4-0a39ce100556">ICameraControl::getRange_PanRelative</a>.

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
<td>Stopped.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Panning to the right.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Panning to the left.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

