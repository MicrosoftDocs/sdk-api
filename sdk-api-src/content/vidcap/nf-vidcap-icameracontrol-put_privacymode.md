---
UID: NF:vidcap.ICameraControl.put_PrivacyMode
title: ICameraControl::put_PrivacyMode
author: windows-sdk-content
description: The put_PrivacyMode method sets the camera's privacy setting. The privacy setting controls whether the camera sensor captures video.
old-location: dshow\icameracontrol_put_privacymode.htm
tech.root: DirectShow
ms.assetid: 04116eba-926c-43fc-9a45-91be42e9af26
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICameraControl interface [DirectShow],put_PrivacyMode method, ICameraControl.put_PrivacyMode, ICameraControl::put_PrivacyMode, ICameraControlput_PrivacyMode, dshow.icameracontrol_put_privacymode, put_PrivacyMode, put_PrivacyMode method [DirectShow], put_PrivacyMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_PrivacyMode
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
 - ICameraControl.put_PrivacyMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICameraControl::put_PrivacyMode


## -description


The <code>put_PrivacyMode</code> method sets the camera's privacy setting. The privacy setting controls whether the camera sensor captures video.


## -parameters




### -param Value [in]

Specifies one of the following values.

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
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

