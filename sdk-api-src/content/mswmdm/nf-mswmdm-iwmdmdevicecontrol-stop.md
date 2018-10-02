---
UID: NF:mswmdm.IWMDMDeviceControl.Stop
title: IWMDMDeviceControl::Stop
author: windows-sdk-content
description: The Stop method stops the current record or play operation.
old-location: wmdm\iwmdmdevicecontrol_stop.htm
tech.root: WMDM
ms.assetid: 842b7de7-dde2-40d1-8028-9ffebcaea90e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWMDMDeviceControl interface [windows Media Device Manager],Stop method, IWMDMDeviceControl.Stop, IWMDMDeviceControl::Stop, IWMDMDeviceControlStop, Stop, Stop method [windows Media Device Manager], Stop method [windows Media Device Manager],IWMDMDeviceControl interface, mswmdm/IWMDMDeviceControl::Stop, wmdm.iwmdmdevicecontrol_stop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWMDMDeviceControl.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDeviceControl::Stop


## -description



The <b>Stop</b> method stops the current record or play operation.




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




<a href="https://msdn.microsoft.com/e7b58957-4795-461f-ae3d-fb80e6711c9f">IWMDMDeviceControl Interface</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

