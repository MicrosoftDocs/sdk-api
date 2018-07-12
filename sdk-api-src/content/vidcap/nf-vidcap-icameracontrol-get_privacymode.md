---
UID: NF:vidcap.ICameraControl.get_PrivacyMode
title: ICameraControl::get_PrivacyMode
author: windows-sdk-content
description: "."
old-location: dshow\icameracontrol_get_privacymode.htm
old-project: DirectShow
ms.assetid: 22bec1da-65ca-4101-8f30-8fbb537e5678
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ICameraControl interface [DirectShow],get_PrivacyMode method, ICameraControl.get_PrivacyMode, ICameraControl::get_PrivacyMode, ICameraControlget_PrivacyMode, dshow.icameracontrol_get_privacymode, get_PrivacyMode, get_PrivacyMode method [DirectShow], get_PrivacyMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PrivacyMode
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
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
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICameraControl::get_PrivacyMode


## -description




The <code>get_PrivacyMode</code> method returns the camera's privacy setting. The privacy setting controls whether camera sensor captures video.


## -parameters




### -param pValue [out]

Receives one of the following values.

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
<td>The sensor is able to capture video.</td>
</tr>
<tr>
<td>1</td>
<td>The sensor is not able to capture video.</td>
</tr>
</table>
 


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

