---
UID: NF:mswmdm.IMDSPDeviceControl.Stop
title: IMDSPDeviceControl::Stop (mswmdm.h)
author: windows-sdk-content
description: The Stop method stops the current stream.
old-location: wmdm\imdspdevicecontrol_stop.htm
tech.root: WMDM
ms.assetid: 31dd1325-2a8d-4a61-a4a5-f585b320e841
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPDeviceControl interface [windows Media Device Manager],Stop method, IMDSPDeviceControl.Stop, IMDSPDeviceControl::Stop, IMDSPDeviceControlStop, Stop, Stop method [windows Media Device Manager], Stop method [windows Media Device Manager],IMDSPDeviceControl interface, mswmdm/IMDSPDeviceControl::Stop, wmdm.imdspdevicecontrol_stop
ms.topic: method
f1_keywords: 
 - "mswmdm/IMDSPDeviceControl.Stop"
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDeviceControl.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPDeviceControl::Stop


## -description



The <b>Stop</b> method stops the current stream.




## -parameters






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
<dt><b>E_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The device is busy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The stop function is not implemented on this device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol">IWMDMDeviceControl Interface</a>
 

 

