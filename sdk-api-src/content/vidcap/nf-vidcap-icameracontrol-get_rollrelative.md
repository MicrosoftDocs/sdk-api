---
UID: NF:vidcap.ICameraControl.get_RollRelative
title: ICameraControl::get_RollRelative (vidcap.h)
description: The get_RollRelative method returns the camera's relative roll. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_RollRelative method","ICameraControl.get_RollRelative","ICameraControl::get_RollRelative","ICameraControlget_RollRelative","dshow.icameracontrol_get_rollrelative","get_RollRelative","get_RollRelative method [DirectShow]","get_RollRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_RollRelative"]
old-location: dshow\icameracontrol_get_rollrelative.htm
tech.root: DirectShow
ms.assetid: 28fa7e55-8e43-40fc-ac6c-e19f91621405
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_RollRelative method, ICameraControl.get_RollRelative, ICameraControl::get_RollRelative, ICameraControlget_RollRelative, dshow.icameracontrol_get_rollrelative, get_RollRelative, get_RollRelative method [DirectShow], get_RollRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_RollRelative
f1_keywords:
- vidcap/ICameraControl.get_RollRelative
dev_langs:
- c++
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
- ICameraControl.get_RollRelative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_RollRelative


## -description


The <code>get_RollRelative</code> method returns the camera's relative roll. The relative roll is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pValue [out]

Receives the relative roll. The size of the value represents the desired rotation speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_rollrelative">ICameraControl::getRange_RollRelative</a>.

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
<td>Rotating clockwise around the viewing axis.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Rotating counterclockwise around the viewing axis.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

