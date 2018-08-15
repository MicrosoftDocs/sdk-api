---
UID: NF:mfidl.IMFSensorProcessActivity.GetStreamingMode
title: IMFSensorProcessActivity::GetStreamingMode
author: windows-sdk-content
description: Gets the streaming mode of the sensor process.
old-location: mf\imfsensorprocessactivity_getstreamingmode.htm
old-project: medfound
ms.assetid: 1881652A-005C-4EFB-B4ED-3BEAC35A460A
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetStreamingMode, GetStreamingMode method [Media Foundation], GetStreamingMode method [Media Foundation],IMFSensorProcessActivity interface, IMFSensorProcessActivity interface [Media Foundation],GetStreamingMode method, IMFSensorProcessActivity.GetStreamingMode, IMFSensorProcessActivity::GetStreamingMode, mf.imfsensorprocessactivity_getstreamingmode, mfidl/IMFSensorProcessActivity::GetStreamingMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorProcessActivity.GetStreamingMode
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProcessActivity::GetStreamingMode


## -description


Gets the streaming mode of the sensor process.


## -parameters




### -param pMode [out]

Receives the process ID.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pMode</i> parameter is null.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a>
 

 

