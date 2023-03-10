---
UID: NF:vidcap.ICameraControl.get_Focus
title: ICameraControl::get_Focus (vidcap.h)
description: The get_Focus method returns the distance that is optimally in focus.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_Focus method","ICameraControl.get_Focus","ICameraControl::get_Focus","ICameraControlget_Focus","dshow.icameracontrol_get_focus","get_Focus","get_Focus method [DirectShow]","get_Focus method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_Focus"]
old-location: dshow\icameracontrol_get_focus.htm
tech.root: dshow
ms.assetid: 59ab6306-539f-4be4-8e69-348eab6220ea
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_Focus method, ICameraControl.get_Focus, ICameraControl::get_Focus, ICameraControlget_Focus, dshow.icameracontrol_get_focus, get_Focus, get_Focus method [DirectShow], get_Focus method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_Focus
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
 - ICameraControl::get_Focus
 - vidcap/ICameraControl::get_Focus
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
 - ICameraControl.get_Focus
---

# ICameraControl::get_Focus


## -description

The <code>get_Focus</code> method returns the distance that is optimally in focus.

## -parameters

### -param pValue [out]

Receives the distance that is in focus, in millimeters.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>