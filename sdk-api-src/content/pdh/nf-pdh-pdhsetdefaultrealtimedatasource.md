---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PdhSetDefaultRealTimeDataSource function


## -description



			Specifies the source of the real-time data.
		


## -parameters




### -param dwDataSourceId [in]

Source of the performance data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DATA_SOURCE_REGISTRY"></a><a id="data_source_registry"></a><dl>
<dt><b>DATA_SOURCE_REGISTRY</b></dt>
</dl>
</td>
<td width="60%">
The data source is the registry interface. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="DATA_SOURCE_WBEM"></a><a id="data_source_wbem"></a><dl>
<dt><b>DATA_SOURCE_WBEM</b></dt>
</dl>
</td>
<td width="60%">
The data source is a WMI provider.

</td>
</tr>
</table>
 


## -returns




						If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> or a 
<a href="https://msdn.microsoft.com/ea67d798-81db-44ad-b0fb-24e0c3be7388">PDH error code</a>. The following is a possible value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PDH_INVALID_ARGUMENT</b></dt>
</dl>
</td>
<td width="60%">
The parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



The term <i>real-time</i> as used in the description of this function does not imply the standard meaning of the term <i>real-time</i>. Instead, it describes the collection of performance data from a source providing current information (for example, the registry or a WMI provider) rather than from a log file.

If you want to query real-time data from WMI, you must call <b>PdhSetDefaultRealTimeDataSource</b> to set the default real-time data source. You must call this function before calling any other PDH API function.




## -see-also




<a href="https://msdn.microsoft.com/211d4504-e1f9-48a0-8ddd-613f2f183c59">PdhSelectDataSource</a>
 

 

