---
UID: NE:wsbonline._WSB_OB_STATUS_ENTRY_PAIR_TYPE
title: WSB_OB_STATUS_ENTRY_PAIR_TYPE (wsbonline.h)
author: windows-sdk-content
description: Indicates the type of the parameter value.
old-location: wsb\wsb_ob_status_entry_pair_type.htm
tech.root: wsb
ms.assetid: E2D70C01-D331-4FBC-8586-2878513618D5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSB_OB_ET_DATETIME, WSB_OB_ET_MAX, WSB_OB_ET_NUMBER, WSB_OB_ET_SIZE, WSB_OB_ET_STRING, WSB_OB_ET_TIME, WSB_OB_ET_UNDEFINED, WSB_OB_STATUS_ENTRY_PAIR_TYPE, WSB_OB_STATUS_ENTRY_PAIR_TYPE enumeration [Windows Server Backup], wsb.wsb_ob_status_entry_pair_type, wsbonline/WSB_OB_ET_DATETIME, wsbonline/WSB_OB_ET_MAX, wsbonline/WSB_OB_ET_NUMBER, wsbonline/WSB_OB_ET_SIZE, wsbonline/WSB_OB_ET_STRING, wsbonline/WSB_OB_ET_TIME, wsbonline/WSB_OB_ET_UNDEFINED, wsbonline/WSB_OB_STATUS_ENTRY_PAIR_TYPE
ms.topic: enum
req.header: wsbonline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - WsbOnline.h
api_name:
 - WSB_OB_STATUS_ENTRY_PAIR_TYPE
product: Windows
targetos: Windows
req.typenames: WSB_OB_STATUS_ENTRY_PAIR_TYPE
req.redist: 
ms.custom: 19H1
---

# WSB_OB_STATUS_ENTRY_PAIR_TYPE enumeration


## -description


The <b>WSB_OB_STATUS_ENTRY_PAIR_TYPE</b> enumeration indicates the type of the parameter value contained in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wsbonline/ns-wsbonline-_wsb_ob_status_entry_value_type_pair">WSB_OB_STATUS_ENTRY_VALUE_TYPE_PAIR</a> structure.


## -enum-fields




### -field WSB_OB_ET_UNDEFINED

The value type is undefined.


### -field WSB_OB_ET_STRING

The value type is string.


### -field WSB_OB_ET_NUMBER

The value type is integer.


### -field WSB_OB_ET_DATETIME

The value type is datetime which represents an instant in time, typically expressed as a date and time of day. All time-related values are specified in Coordinated Universal Time (UTC) format.


### -field WSB_OB_ET_TIME

The value type is time. All time-related values are specified in UTC format.


### -field WSB_OB_ET_SIZE

The value type is size.


### -field WSB_OB_ET_MAX

The maximum enumeration value for this enumeration.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wsb/windows-server-backup-api-enumerations">Cloud Backup Provider API Enumerations</a>
 

 

