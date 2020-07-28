---
UID: NF:vidcap.ICameraControl.get_TiltRelative
title: ICameraControl::get_TiltRelative (vidcap.h)
description: This topic applies only to Windows XP Service Pack 2 and later.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_TiltRelative method","ICameraControl.get_TiltRelative","ICameraControl::get_TiltRelative","ICameraControlget_TiltRelative","dshow.icameracontrol_get_tiltrelative","get_TiltRelative","get_TiltRelative method [DirectShow]","get_TiltRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_TiltRelative"]
old-location: dshow\icameracontrol_get_tiltrelative.htm
tech.root: dshow
ms.assetid: e8730043-a506-4c74-a9ca-94d6e003a4b1
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_TiltRelative method, ICameraControl.get_TiltRelative, ICameraControl::get_TiltRelative, ICameraControlget_TiltRelative, dshow.icameracontrol_get_tiltrelative, get_TiltRelative, get_TiltRelative method [DirectShow], get_TiltRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_TiltRelative
f1_keywords:
- vidcap/ICameraControl.get_TiltRelative
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
- ICameraControl.get_TiltRelative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_TiltRelative


## -description



This topic applies only to Windows XP Service Pack 2 and later.
        



The <code>get_TiltRelative</code> method returns the camera's relative tilt. The relative tilt is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pValue [out]

Receives the relative tilt. The size of the value represents the desired tilt speed; a higher value represents a higher speed. To get the range of possible values, call <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_tiltrelative">ICameraControl::getRange_TiltRelative</a>.

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
<td>Tilting up.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Tilting down.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

