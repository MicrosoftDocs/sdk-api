---
UID: NF:vidcap.ICameraControl.get_ExposureRelative
title: ICameraControl::get_ExposureRelative (vidcap.h)
description: The get_ExposureRelative method returns the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_ExposureRelative method","ICameraControl.get_ExposureRelative","ICameraControl::get_ExposureRelative","ICameraControlget_ExposureRelative","dshow.icameracontrol_get_exposurerelative","get_ExposureRelative","get_ExposureRelative method [DirectShow]","get_ExposureRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_ExposureRelative"]
old-location: dshow\icameracontrol_get_exposurerelative.htm
tech.root: DirectShow
ms.assetid: d63cf869-ccb6-45cb-85ba-a1e41faa8086
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_ExposureRelative method, ICameraControl.get_ExposureRelative, ICameraControl::get_ExposureRelative, ICameraControlget_ExposureRelative, dshow.icameracontrol_get_exposurerelative, get_ExposureRelative, get_ExposureRelative method [DirectShow], get_ExposureRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ExposureRelative
f1_keywords:
- vidcap/ICameraControl.get_ExposureRelative
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
- ICameraControl.get_ExposureRelative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_ExposureRelative


## -description


The <code>get_ExposureRelative</code> method returns the camera's relative exposure time. The relative exposure time is expressed as a number of steps, where the size of each step depends on the camera model.


## -parameters




### -param pValue [out]

Receives the relative exposure. To get the range of possible values, call <a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_exposurerelative">ICameraControl::getRange_ExposureRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
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

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

