---
UID: NF:sensorsapi.ISensorDataReport.GetTimestamp
title: ISensorDataReport::GetTimestamp
author: windows-sdk-content
description: Retrieves the time at which the data report was created.
old-location: winsensors_com_ref\isensordatareport_gettimestamp.htm
tech.root: SensorsAPI
ms.assetid: 3366bfb5-1132-4960-8a0e-49967310ade5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTimestamp, GetTimestamp method, GetTimestamp method,ISensorDataReport interface, ISensorDataReport interface,GetTimestamp method, ISensorDataReport.GetTimestamp, ISensorDataReport::GetTimestamp, sensorsapi/ISensorDataReport::GetTimestamp, winsensors_com_ref.isensordatareport_gettimestamp
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISensorDataReport.GetTimestamp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISensorDataReport::GetTimestamp


## -description


Retrieves the time at which the data report was created.


## -parameters




### -param pTimeStamp [out]

Address of a <a href="http://go.microsoft.com/fwlink/p/?linkid=157229">SYSTEMTIME</a> variable that receives the time stamp. 


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
The sensor driver did not return a valid time stamp for the data report.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pTimeStamp.

</td>
</tr>
</table>
 




## -remarks



Time stamps use Universal Coordinated Time (UTC).




## -see-also




<a href="https://msdn.microsoft.com/c677b956-e3ab-477c-b97b-aceec4e2d235">ISensorDataReport</a>
 

 

