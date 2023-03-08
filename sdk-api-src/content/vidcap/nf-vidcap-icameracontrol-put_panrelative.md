---
UID: NF:vidcap.ICameraControl.put_PanRelative
title: ICameraControl::put_PanRelative (vidcap.h)
description: The put_PanRelative method sets the camera's relative pan. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_PanRelative method","ICameraControl.put_PanRelative","ICameraControl::put_PanRelative","ICameraControlput_PanRelative","dshow.icameracontrol_put_panrelative","put_PanRelative","put_PanRelative method [DirectShow]","put_PanRelative method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_PanRelative"]
old-location: dshow\icameracontrol_put_panrelative.htm
tech.root: dshow
ms.assetid: a4ac28f4-8570-4307-80c1-2960d7c87544
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],put_PanRelative method, ICameraControl.put_PanRelative, ICameraControl::put_PanRelative, ICameraControlput_PanRelative, dshow.icameracontrol_put_panrelative, put_PanRelative, put_PanRelative method [DirectShow], put_PanRelative method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_PanRelative
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
 - ICameraControl::put_PanRelative
 - vidcap/ICameraControl::put_PanRelative
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
 - ICameraControl.put_PanRelative
---

# ICameraControl::put_PanRelative


## -description

The <code>put_PanRelative</code> method sets the camera's relative pan. The relative pan is expressed as a number of steps, where the size of each step depends on the camera model.

## -parameters

### -param Value [in]

Specifies the relative pan. The size of the value represents the desired pan speed; a higher value represents a higher speed. To get the range of possible values, call <a href="/windows/desktop/api/vidcap/nf-vidcap-icameracontrol-getrange_panrelative">ICameraControl::getRange_PanRelative</a>.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Stop panning.</td>
</tr>
<tr>
<td>Positive value</td>
<td>Start panning to the right.</td>
</tr>
<tr>
<td>Negative value</td>
<td>Start panning to the left.</td>
</tr>
</table>

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>