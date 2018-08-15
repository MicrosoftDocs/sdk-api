---
UID: NF:sensorsapi.ISensorDataReport.GetSensorValues
title: ISensorDataReport::GetSensorValues
author: windows-sdk-content
description: Retrieves a collection of data field values.
old-location: winsensors_com_ref\isensordatareport_getsensorvalues.htm
old-project: SensorsAPI
ms.assetid: d7450caf-9b82-41ee-9ea2-d8f4502473ce
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSensorValues, GetSensorValues method, GetSensorValues method,ISensorDataReport interface, ISensorDataReport interface,GetSensorValues method, ISensorDataReport.GetSensorValues, ISensorDataReport::GetSensorValues, sensorsapi/ISensorDataReport::GetSensorValues, winsensors_com_ref.isensordatareport_getsensorvalues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensorsapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: SensorConnectionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorDataReport.GetSensorValues
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
---

# ISensorDataReport::GetSensorValues


## -description


Retrieves a collection of data field values.


## -parameters




### -param pKeys [in]

Pointer to the <a href="http://go.microsoft.com/fwlink/p/?linkid=134661">IPortableDeviceKeyCollection</a> interface that contains the data fields for which to retrieve values. Set to <b>NULL</b> to retrieve values for all supported data fields.


### -param ppValues [out]

Address of an <a href="http://go.microsoft.com/fwlink/p/?linkid=134660">IPortableDeviceValues</a> interface pointer that receives the pointer to the retrieved values.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)
</b></dt>
</dl>
</td>
<td width="60%">
A data field was not found. Inspect <i>ppValues</i> to determine which values were set to <b>ERROR_NOT_FOUND</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for ppValues.

</td>
</tr>
</table>
 




## -remarks



The <b>IPortableDeviceKeyCollection</b> and <b>IPortableDeviceValues</b> interfaces are defined by the Windows Portable Devices API.

When this method returns <b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b>, one or more of the results contained by the <a href="http://go.microsoft.com/fwlink/p/?linkid=134660">IPortableDeviceValues</a> interface will be set to an <b>HRESULT</b> error value.




## -see-also




<a href="https://msdn.microsoft.com/c677b956-e3ab-477c-b97b-aceec4e2d235">ISensorDataReport</a>
 

 

