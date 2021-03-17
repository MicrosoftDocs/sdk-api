---
UID: NE:sdoias._ACCOUNTINGPROPERTIES
title: ACCOUNTINGPROPERTIES (sdoias.h)
description: The values of the ACCOUNTINGPROPERTIES type enumerate properties that control what types of packets are logged and characteristics of the log file.
helpviewer_keywords: ["ACCOUNTINGPROPERTIES","ACCOUNTINGPROPERTIES enumeration [Network Policy Server]","PROPERTY_ACCOUNTING_LOG_ACCOUNTING","PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM","PROPERTY_ACCOUNTING_LOG_AUTHENTICATION","PROPERTY_ACCOUNTING_LOG_AUTHENTICATION_INTERIM","PROPERTY_ACCOUNTING_LOG_DELETE_IF_FULL","PROPERTY_ACCOUNTING_LOG_ENABLE","PROPERTY_ACCOUNTING_LOG_ENABLE_LOGGING","PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY","PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT","PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY","PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE","PROPERTY_ACCOUNTING_SQL_MAX_SESSIONS","_sdo_accountingproperties","nps.SDO_accountingproperties","sdo.accountingproperties","sdoias/ACCOUNTINGPROPERTIES","sdoias/PROPERTY_ACCOUNTING_LOG_ACCOUNTING","sdoias/PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM","sdoias/PROPERTY_ACCOUNTING_LOG_AUTHENTICATION","sdoias/PROPERTY_ACCOUNTING_LOG_AUTHENTICATION_INTERIM","sdoias/PROPERTY_ACCOUNTING_LOG_DELETE_IF_FULL","sdoias/PROPERTY_ACCOUNTING_LOG_ENABLE","sdoias/PROPERTY_ACCOUNTING_LOG_ENABLE_LOGGING","sdoias/PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY","sdoias/PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT","sdoias/PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY","sdoias/PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE","sdoias/PROPERTY_ACCOUNTING_SQL_MAX_SESSIONS"]
old-location: nps\SDO_accountingproperties.htm
tech.root: Nps
ms.assetid: e814d576-0405-410e-ae62-e0f5905f6cf9
ms.date: 12/05/2018
ms.keywords: ACCOUNTINGPROPERTIES, ACCOUNTINGPROPERTIES enumeration [Network Policy Server], PROPERTY_ACCOUNTING_LOG_ACCOUNTING, PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM, PROPERTY_ACCOUNTING_LOG_AUTHENTICATION, PROPERTY_ACCOUNTING_LOG_AUTHENTICATION_INTERIM, PROPERTY_ACCOUNTING_LOG_DELETE_IF_FULL, PROPERTY_ACCOUNTING_LOG_ENABLE, PROPERTY_ACCOUNTING_LOG_ENABLE_LOGGING, PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY, PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT, PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY, PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE, PROPERTY_ACCOUNTING_SQL_MAX_SESSIONS, _sdo_accountingproperties, nps.SDO_accountingproperties, sdo.accountingproperties, sdoias/ACCOUNTINGPROPERTIES, sdoias/PROPERTY_ACCOUNTING_LOG_ACCOUNTING, sdoias/PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM, sdoias/PROPERTY_ACCOUNTING_LOG_AUTHENTICATION, sdoias/PROPERTY_ACCOUNTING_LOG_AUTHENTICATION_INTERIM, sdoias/PROPERTY_ACCOUNTING_LOG_DELETE_IF_FULL, sdoias/PROPERTY_ACCOUNTING_LOG_ENABLE, sdoias/PROPERTY_ACCOUNTING_LOG_ENABLE_LOGGING, sdoias/PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY, sdoias/PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT, sdoias/PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY, sdoias/PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE, sdoias/PROPERTY_ACCOUNTING_SQL_MAX_SESSIONS
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACCOUNTINGPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACCOUNTINGPROPERTIES
 - sdoias/_ACCOUNTINGPROPERTIES
 - ACCOUNTINGPROPERTIES
 - sdoias/ACCOUNTINGPROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - ACCOUNTINGPROPERTIES
---

# ACCOUNTINGPROPERTIES enumeration


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
<a href="/windows/desktop/api/sdoias/ne-sdoias-new_log_file_frequency">NEW_LOG_FILE_FREQUENCY</a> enumeration type.

### -field PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE

Specifies a file size. The system creates a new log file if the current log file reaches this size, and the <b>PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY</b> property is set to the value 
<a href="/windows/desktop/api/sdoias/ne-sdoias-new_log_file_frequency">IAS_LOGGING_WHEN_FILE_SIZE_REACHES</a>.

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

<a href="/previous-versions/windows/desktop/automat/oleautomation">Automation Types</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-new_log_file_frequency">NEW_LOG_FILE_FREQUENCY</a>



<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>