---
UID: NF:evr.IMFVideoDeviceID.GetDeviceID
title: IMFVideoDeviceID::GetDeviceID (evr.h)
author: windows-sdk-content
description: Returns the identifier of the video device supported by an EVR mixer or presenter.
old-location: mf\imfvideodeviceid_getdeviceid.htm
tech.root: medfound
ms.assetid: e23ebce0-be58-413a-ab71-d94811c96029
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDeviceID, GetDeviceID method [Media Foundation], GetDeviceID method [Media Foundation],IMFVideoDeviceID interface, IMFVideoDeviceID interface [Media Foundation],GetDeviceID method, IMFVideoDeviceID.GetDeviceID, IMFVideoDeviceID::GetDeviceID, e23ebce0-be58-413a-ab71-d94811c96029, evr/IMFVideoDeviceID::GetDeviceID, mf.imfvideodeviceid_getdeviceid
ms.topic: method
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDeviceID.GetDeviceID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoDeviceID::GetDeviceID


## -description



Returns the identifier of the video device supported by an EVR mixer or presenter.




## -parameters




### -param pDeviceID [out]

Receives the device identifier. Generally, the value is IID_IDirect3DDevice9.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>
 




## -remarks



If a mixer or presenter uses Direct3D 9, it must return the value IID_IDirect3DDevice9 in <i>pDeviceID</i>. The EVR's default mixer and presenter both return this value. If you write a custom mixer or presenter, it can return some other value. However, the mixer and presenter must use matching device identifiers.




## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/c42b75f9-6b72-4aab-92f2-3361ab475ce9">IMFVideoDeviceID</a>
 

 

