---
UID: NF:mfidl.IMFSensorProcessActivity.GetStreamingMode
title: IMFSensorProcessActivity::GetStreamingMode (mfidl.h)
description: Gets the streaming mode of the sensor process.
helpviewer_keywords: ["GetStreamingMode","GetStreamingMode method [Media Foundation]","GetStreamingMode method [Media Foundation]","IMFSensorProcessActivity interface","IMFSensorProcessActivity interface [Media Foundation]","GetStreamingMode method","IMFSensorProcessActivity.GetStreamingMode","IMFSensorProcessActivity::GetStreamingMode","mf.imfsensorprocessactivity_getstreamingmode","mfidl/IMFSensorProcessActivity::GetStreamingMode"]
old-location: mf\imfsensorprocessactivity_getstreamingmode.htm
tech.root: mf
ms.assetid: 1881652A-005C-4EFB-B4ED-3BEAC35A460A
ms.date: 12/05/2018
ms.keywords: GetStreamingMode, GetStreamingMode method [Media Foundation], GetStreamingMode method [Media Foundation],IMFSensorProcessActivity interface, IMFSensorProcessActivity interface [Media Foundation],GetStreamingMode method, IMFSensorProcessActivity.GetStreamingMode, IMFSensorProcessActivity::GetStreamingMode, mf.imfsensorprocessactivity_getstreamingmode, mfidl/IMFSensorProcessActivity::GetStreamingMode
req.header: mfidl.h
req.include-header: 
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorProcessActivity::GetStreamingMode
 - mfidl/IMFSensorProcessActivity::GetStreamingMode
dev_langs:
 - c++
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
---

# IMFSensorProcessActivity::GetStreamingMode


## -description

Gets the streaming mode of the sensor process.

## -parameters

### -param pMode [out]

Receives a value from the MFSensorDeviceMode enumeration specifying the streaming mode of the sensor process.

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
<a href="/windows/desktop/api/mfidl/ne-mfidl-mfsensordevicemode">MFSensorDeviceMode</a> 
<p>
<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a>