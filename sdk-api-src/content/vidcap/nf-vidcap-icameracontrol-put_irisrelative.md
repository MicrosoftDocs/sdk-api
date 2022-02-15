---
UID: NF:vidcap.ICameraControl.put_IrisRelative
title: ICameraControl::put_IrisRelative (vidcap.h)
description: The put_IrisRelative method sets the camera's relative aperture setting. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_IrisRelative method","ICameraControl.put_IrisRelative","ICameraControl::put_IrisRelative","ICameraControlput_IrisRelative","dshow.icameracontrol_put_irisrelative","put_IrisRelative","put_IrisRelative method [DirectShow]","put_IrisRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_IrisRelative"]
old-location: dshow\icameracontrol_put_irisrelative.htm
tech.root: dshow
ms.assetid: 76cd3b1d-a6ce-4981-b82f-7ee83e118c33
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_IrisRelative method, ICameraControl.put_IrisRelative, ICameraControl::put_IrisRelative, ICameraControlput_IrisRelative, dshow.icameracontrol_put_irisrelative, put_IrisRelative, put_IrisRelative method [DirectShow], put_IrisRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_IrisRelative
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICameraControl::put_IrisRelative
 - vidcap/ICameraControl::put_IrisRelative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.put_IrisRelative
---

# ICameraControl::put_IrisRelative


## -description

The <code>put_IrisRelative</code> method sets the camera's relative aperture setting. The relative aperture is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param Value [in]

Specifies the relative aperture setting. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_irisrelative">ICameraControl::getRange_IrisRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Set the default aperture setting, which is implementation dependent.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Open the iris one step.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Close the iris one step.</td>
</tr>
</table>

### -param Flags [in]

Zero or more flags. See <a href="/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>