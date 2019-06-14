---
UID: NE:sdoias._NEW_LOG_FILE_FREQUENCY
title: NEW_LOG_FILE_FREQUENCY (sdoias.h)
author: windows-sdk-content
description: The values of the NEW_LOG_FILE_FREQUENCY enumeration type specify how frequently new log files are created.
old-location: nps\SDO_new_log_file_frequency.htm
tech.root: Nps
ms.assetid: d051ff06-f425-49e5-ac29-6d7873174eb7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAS_LOGGING_DAILY, IAS_LOGGING_MONTHLY, IAS_LOGGING_UNLIMITED_SIZE, IAS_LOGGING_WEEKLY, IAS_LOGGING_WHEN_FILE_SIZE_REACHES, NEW_LOG_FILE_FREQUENCY, NEW_LOG_FILE_FREQUENCY enumeration [Network Policy Server], _sdo_new_log_file_frequency, nps.SDO_new_log_file_frequency, sdo.new_log_file_frequency, sdoias/IAS_LOGGING_DAILY, sdoias/IAS_LOGGING_MONTHLY, sdoias/IAS_LOGGING_UNLIMITED_SIZE, sdoias/IAS_LOGGING_WEEKLY, sdoias/IAS_LOGGING_WHEN_FILE_SIZE_REACHES, sdoias/NEW_LOG_FILE_FREQUENCY
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - NEW_LOG_FILE_FREQUENCY
product: Windows
targetos: Windows
req.typenames: NEW_LOG_FILE_FREQUENCY
req.redist: 
ms.custom: 19H1
---

# NEW_LOG_FILE_FREQUENCY enumeration


## -description


The values of the 
<b>NEW_LOG_FILE_FREQUENCY</b> enumeration type specify how frequently new log files are created.


## -enum-fields




### -field IAS_LOGGING_UNLIMITED_SIZE

Allows the log file to grow without limit. Do not create new log files periodically.


### -field IAS_LOGGING_DAILY

Creates a new log file each day.


### -field IAS_LOGGING_WEEKLY

Creates a new log file each week.


### -field IAS_LOGGING_MONTHLY

Creates a new log file each month.


### -field IAS_LOGGING_WHEN_FILE_SIZE_REACHES

Creates a new log file when the log file reaches a particular size.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/ne-sdoias-_accountingproperties">ACCOUNTINGPROPERTIES</a>
 

 

