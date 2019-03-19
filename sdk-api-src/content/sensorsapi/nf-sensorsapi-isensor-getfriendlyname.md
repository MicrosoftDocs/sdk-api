---
UID: NF:sensorsapi.ISensor.GetFriendlyName
title: ISensor::GetFriendlyName (sensorsapi.h)
author: windows-sdk-content
description: Retrieves the sensor name that is intended to be seen by the user.
old-location: winsensors_com_ref\isensor_getfriendlyname.htm
tech.root: SensorsAPI
ms.assetid: 380a1a93-01f7-4d5b-9916-156728fd94ed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFriendlyName, GetFriendlyName method, GetFriendlyName method,ISensor interface, ISensor interface,GetFriendlyName method, ISensor.GetFriendlyName, ISensor::GetFriendlyName, sensorsapi/ISensor::GetFriendlyName, winsensors_com_ref.isensor_getfriendlyname
ms.topic: method
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
 - ISensor.GetFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensor::GetFriendlyName


## -description


Retrieves the sensor name that is intended to be seen by the user.


## -parameters




### -param pFriendlyName [out]

Address of a <b>BSTR</b> that receives the friendly name.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The sensor driver did not provide a friendly name value. The value provided through <i>pFriendlyName</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pFriendlyName.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3216afbb-d524-486d-99ad-0ee0cfb884e0">ISensor</a>
 

 

