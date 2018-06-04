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

# PerfQueryCounterSetRegistrationInfo function


## -description


Gets information about a counter set on the specified system.



## -parameters




### -param szMachine [in, optional]

The name of the machine for which to get the information about the counter set  that the <i>pCounterSet</i> parameter specifies. If NULL, the function retrieves information about the specified counter set for the local machine.


### -param pCounterSetId [in]

The counter set identifier of the counter set for which you want to get information.


### -param requestCode

The type of information that you want to get about the counter set. See <a href="https://msdn.microsoft.com/8D54F31F-9ABA-405F-84A5-9C7225B7BE67">PerfRegInfoType</a> for a list of possible values.


### -param requestLangId

The preferred locale identifier for the strings that contain the requested information if <i>requestCode</i> is <b>PERF_REG_COUNTERSET_NAME_STRING</b>,  

<b>PERF_REG_COUNTERSET_HELP_STRING</b>, <b>PERF_REG_COUNTER_NAME_STRINGS</b>, or  

<b>PERF_REG_COUNTER_HELP_STRINGS</b>.

The counter identifier of the counter for which you want data, if <i>requestCode</i> is <b>PERF_REG_COUNTER_STRUCT</b>. 

Set to 0 for all other values of <i>requestCode</i>.


### -param pbRegInfo [out, optional]

Pointer to a buffer that is large enough to receive the amount of data that the <i>cbRegInfo</i> parameter specifies, in bytes. May be  

NULL if <i>cbRegInfo</i> is 0.  



### -param cbRegInfo

The size of the buffer that the <i>pbRegInfo</i> parameter specifies, in bytes.  



### -param pcbRegInfoActual [out]

The size of the buffer actually required to get the information about the counter set. The meaning depends on the value that the function  

returns.

<table>
<tr>
<th>Function  Return Value</th>
<th>Meaning of <i>pcbRegInfoActual</i></th>
</tr>
<tr>
<td><b>ERROR_SUCCESS</b></td>
<td>The number of  

  bytes of information about the specified counter set that the function stored in the buffer that <i>pbRegInfo</i> specified.</td>
</tr>
<tr>
<td><b> ERROR_NOT_ENOUGH_MEMORY</b></td>
<td>The  

  size of the buffer required to store the information about the counter set on the specified machine, in bytes. Enlarge the buffer to the required  

  size and call the function again.  

</td>
</tr>
<tr>
<td>Other</td>
<td>The value is undefined and should not be used.</td>
</tr>
</table>
 


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function successfully stored all of the information about the counter set in the buffer that <i>pbRegInfo</i> specified. The value that <i>pcbRegInfoActual</i> points to indicates amount of information actually stored in the buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
 The buffer that <i>pbRegInfo</i> specified was not large enough to store all of the information about the counter set.  The value that <i>pcbRegInfoActual</i> points to  indicates the size of the buffer required to store all of the information. Enlarge the buffer to the required  

  size and call the function again.  



</td>
</tr>
</table>
 


						
						For other types of failures, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. 
					




## -remarks



See  <a href="https://msdn.microsoft.com/8D54F31F-9ABA-405F-84A5-9C7225B7BE67">PerfRegInfoType</a>  for the types of data that you can request and  

the formats of the data provided for each type of request. 




