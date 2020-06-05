---
UID: NF:vidcap.ICameraControl.get_PrivacyMode
title: ICameraControl::get_PrivacyMode (vidcap.h)
description: .helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_PrivacyMode method","ICameraControl.get_PrivacyMode","ICameraControl::get_PrivacyMode","ICameraControlget_PrivacyMode","dshow.icameracontrol_get_privacymode","get_PrivacyMode","get_PrivacyMode method [DirectShow]","get_PrivacyMode method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_PrivacyMode"]
old-location: dshow\icameracontrol_get_privacymode.htm
tech.root: DirectShow
ms.assetid: 22bec1da-65ca-4101-8f30-8fbb537e5678
ms.date: 12/05/2018
ms.keywords: ICameraControl interface [DirectShow],get_PrivacyMode method, ICameraControl.get_PrivacyMode, ICameraControl::get_PrivacyMode, ICameraControlget_PrivacyMode, dshow.icameracontrol_get_privacymode, get_PrivacyMode, get_PrivacyMode method [DirectShow], get_PrivacyMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PrivacyMode
f1_keywords:
- vidcap/ICameraControl.get_PrivacyMode
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
- ICameraControl.get_PrivacyMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICameraControl::get_PrivacyMode


## -description




The <code>get_PrivacyMode</code> method returns the camera's privacy setting. The privacy setting controls whether camera sensor captures video.


## -parameters




### -param pValue [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The sensor is able to capture video.</td>
</tr>
<tr>
<td>1</td>
<td>The sensor is not able to capture video.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>
 

 

