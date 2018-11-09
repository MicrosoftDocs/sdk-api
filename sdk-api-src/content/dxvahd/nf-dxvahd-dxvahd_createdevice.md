---
UID: NF:dxvahd.DXVAHD_CreateDevice
title: DXVAHD_CreateDevice function
author: windows-sdk-content
description: Creates a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_createdevice.htm
tech.root: medfound
ms.assetid: 9a5411f9-2018-4a8a-922d-ab431d615583
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DXVAHD_CreateDevice, DXVAHD_CreateDevice function [Media Foundation], dxvahd/DXVAHD_CreateDevice, mf.dxvahd_createdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - DXVAHD_CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DXVAHD_CreateDevice function


## -description


Creates a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param pD3DDevice [in]

A pointer to the <a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a> interface of a Direct3D 9 device.


### -param pContentDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/9319a98d-8f43-4f29-8787-18dec53dff88">DXVAHD_CONTENT_DESC</a> structure that describes the video content. The driver uses this information as a hint when it creates the device.


### -param Usage [in]

A member of the <a href="https://msdn.microsoft.com/d071dea8-2bab-4768-bdbe-86af08a65dc5">DXVAHD_DEVICE_USAGE</a> enumeration, describing how the device will be used. The value indicates the desired trade-off between speed and video quality. The driver uses this flag as a hint when it creates the device.


### -param pPlugin [in]

A pointer to an initialization function for a software device. Set this pointer if you are using a software plug-in device. Otherwise, set this parameter to <b>NULL</b>. If the value is <b>NULL</b>, the driver creates the DXVA-HD device.

The function pointer type is <a href="https://msdn.microsoft.com/1290daa0-a2dd-4067-b74d-e1b3e3edb321">PDXVAHDSW_Plugin</a>.


### -param ppDevice [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a> interface. The caller must release the interface.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The Direct3D device does not support DXVA-HD.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a> interface to get the device capabilities, create the video processor, and allocate video surfaces.
      




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

