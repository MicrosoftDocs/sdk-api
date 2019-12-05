---
UID: NF:sensorsapi.ISensorDataReport.GetSensorValues
title: ISensorDataReport::GetSensorValues (sensorsapi.h)
description: Retrieves a collection of data field values.
old-location: winsensors_com_ref\isensordatareport_getsensorvalues.htm
tech.root: SensorsAPI
ms.assetid: d7450caf-9b82-41ee-9ea2-d8f4502473ce
ms.date: 12/05/2018
ms.keywords: GetSensorValues, GetSensorValues method, GetSensorValues method,ISensorDataReport interface, ISensorDataReport interface,GetSensorValues method, ISensorDataReport.GetSensorValues, ISensorDataReport::GetSensorValues, sensorsapi/ISensorDataReport::GetSensorValues, winsensors_com_ref.isensordatareport_getsensorvalues
ms.topic: method
f1_keywords:
- sensorsapi/ISensorDataReport.GetSensorValues
dev_langs:
- c++
req.header: sensorsapi.h
req.include-header: 
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
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sensorsapi.dll
api_name:
- ISensorDataReport.GetSensorValues
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport">ISensorDataReport</a>
 

 

