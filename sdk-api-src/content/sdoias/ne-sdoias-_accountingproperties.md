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

# _ACCOUNTINGPROPERTIES enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008. The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The values of the 
<b>ACCOUNTINGPROPERTIES</b> type enumerate properties that control what types of packets are logged and characteristics of the log file.


## -enum-fields




### -field PROPERTY_ACCOUNTING_LOG_ACCOUNTING

Specifies whether accounting packets are logged.


### -field PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM

Specifies whether interim accounting packets are logged.


### -field PROPERTY_ACCOUNTING_LOG_AUTHENTICATION

Specifies whether authentication packets are logged.


### -field PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY

Specifies how frequently a new log file is created. This property takes a value from the 
<a href="https://msdn.microsoft.com/d051ff06-f425-49e5-ac29-6d7873174eb7">NEW_LOG_FILE_FREQUENCY</a> enumeration type.


### -field PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE

Specifies a file size. The system creates a new log file if the current log file reaches this size, and the <b>PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY</b> property is set to the value 
<a href="https://msdn.microsoft.com/d051ff06-f425-49e5-ac29-6d7873174eb7">IAS_LOGGING_WHEN_FILE_SIZE_REACHES</a>.


### -field PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY

The file-system path to the directory where the log file is located. This path does not include the filename. It also does not include a trailing backslash.


### -field PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT

Specifies whether the log should be in NPS format or database convertible format. This property can have the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0 (<b>VARIANT_FALSE</b>)</td>
<td>NPS Format</td>
</tr>
<tr>
<td>0xFFFF (<b>VARIANT_TRUE</b>)</td>
<td>Database Convertible Format</td>
</tr>
</table>
 


### -field PROPERTY_ACCOUNTING_LOG_ENABLE_LOGGING

Not used.


### -field PROPERTY_ACCOUNTING_LOG_DELETE_IF_FULL

Causes the accounting log to be deleted when full.


### -field PROPERTY_ACCOUNTING_SQL_MAX_SESSIONS

Maximum number of concurrent  SQL server sessions.


### -field PROPERTY_ACCOUNTING_LOG_AUTHENTICATION_INTERIM

Causes NPS to log interim access-request/access-challenge pairs for an EAP session. Otherwise, it only logs the final access-request/access-accept/reject.


### -field PROPERTY_ACCOUNTING_LOG_FILE_IS_BACKUP


### -field PROPERTY_ACCOUNTING_DISCARD_REQUEST_ON_FAILURE




#### - PROPERTY_ACCOUNTING_LOG_ENABLE

Not used.


## -see-also




<a href="335e8f55-c313-423e-a301-8ef6a38c5b05">Automation Types</a>



<a href="https://msdn.microsoft.com/d051ff06-f425-49e5-ac29-6d7873174eb7">NEW_LOG_FILE_FREQUENCY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>
 

 

