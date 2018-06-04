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

# SnmpSvcSetLogLevel function


## -description


<p class="CCE_Message">[SNMP is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/6429e748-e0bf-431a-8989-db5b211665d5">Windows Remote Management</a>, which is the Microsoft implementation of WS-Man.]

The
				<b>SnmpSvcSetLogLevel</b> function adjusts the level of detail of the debug output from the SNMP service and from SNMP extension agents using the 
<a href="https://msdn.microsoft.com/ab092155-192f-450f-9635-9c34a4f572aa">SnmpUtilDbgPrint</a> function. This function is an element of the SNMP Utility API.


## -parameters




### -param nLogLevel [in]

Specifies a signed integer variable that indicates the level of detail of the debug output from the 
<a href="https://msdn.microsoft.com/ab092155-192f-450f-9635-9c34a4f572aa">SnmpUtilDbgPrint</a> function. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_SILENT"></a><a id="snmp_log_silent"></a><dl>
<dt><b>SNMP_LOG_SILENT</b></dt>
</dl>
</td>
<td width="60%">
Disable all debugging output.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_FATAL"></a><a id="snmp_log_fatal"></a><dl>
<dt><b>SNMP_LOG_FATAL</b></dt>
</dl>
</td>
<td width="60%">
Display fatal errors only.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_ERROR"></a><a id="snmp_log_error"></a><dl>
<dt><b>SNMP_LOG_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Display recoverable errors.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_WARNING"></a><a id="snmp_log_warning"></a><dl>
<dt><b>SNMP_LOG_WARNING</b></dt>
</dl>
</td>
<td width="60%">
Display warnings and recoverable errors.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_TRACE"></a><a id="snmp_log_trace"></a><dl>
<dt><b>SNMP_LOG_TRACE</b></dt>
</dl>
</td>
<td width="60%">
Display trace information.

</td>
</tr>
<tr>
<td width="40%"><a id="SNMP_LOG_VERBOSE"></a><a id="snmp_log_verbose"></a><dl>
<dt><b>SNMP_LOG_VERBOSE</b></dt>
</dl>
</td>
<td width="60%">
Display verbose trace information.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Extension agents are encouraged to use the 
<a href="https://msdn.microsoft.com/244a8359-9002-4ece-b340-20602d566a2c">SnmpSvcSetLogType</a> and 
<b>SnmpSvcSetLogLevel</b> functions during development to adjust the output of debugging information. Extension agents can integrate the information with the debug output from the SNMP service.




## -see-also




<a href="https://msdn.microsoft.com/8913caa9-6b2c-424c-a778-bd54d6584dac">SNMP Functions</a>



<a href="https://msdn.microsoft.com/499e912b-0821-452e-81f6-8a8250875979">Simple Network Management Protocol (SNMP) Overview</a>



<a href="https://msdn.microsoft.com/244a8359-9002-4ece-b340-20602d566a2c">SnmpSvcSetLogType</a>



<a href="https://msdn.microsoft.com/ab092155-192f-450f-9635-9c34a4f572aa">SnmpUtilDbgPrint</a>
 

 

