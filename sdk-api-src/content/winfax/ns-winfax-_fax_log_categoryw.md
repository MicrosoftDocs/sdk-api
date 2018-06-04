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

# _FAX_LOG_CATEGORYW structure


## -description


The <b>FAX_LOG_CATEGORY</b> structure describes one logging category. The structure contains a logging category name and identifier. It also includes the current level at which the fax server logs events for the specified logging category in the application event log.


## -struct-fields




### -field Name

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is a descriptive name for the logging category.


### -field Category

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a unique value that identifies a logging category. This member can be one of the following predefined values.



#### FAXLOG_CATEGORY_INIT

A fax service initialization or termination event.



#### FAXLOG_CATEGORY_OUTBOUND

An outgoing fax transmission event such as sending a fax.



#### FAXLOG_CATEGORY_INBOUND

An incoming fax transmission event such as receiving a fax or routing a fax.



#### FAXLOG_CATEGORY_UNKNOWN

An unknown event.


### -field Level

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the current logging level for the logging category. This member can be one of the following predefined logging levels.



#### FAXLOG_LEVEL_NONE

The fax server does not log events.



#### FAXLOG_LEVEL_MIN

The fax server logs only the most severe failure events.



#### FAXLOG_LEVEL_MED

The fax server logs most events. (This level does not include some informational and warning events.) 



#### FAXLOG_LEVEL_MAX

The fax server logs all events.


##### - Category.FAXLOG_CATEGORY_INBOUND

An incoming fax transmission event such as receiving a fax or routing a fax.


##### - Category.FAXLOG_CATEGORY_INIT

A fax service initialization or termination event.


##### - Category.FAXLOG_CATEGORY_OUTBOUND

An outgoing fax transmission event such as sending a fax.


##### - Category.FAXLOG_CATEGORY_UNKNOWN

An unknown event.


##### - Level.FAXLOG_LEVEL_MAX

The fax server logs all events.


##### - Level.FAXLOG_LEVEL_MED

The fax server logs most events. (This level does not include some informational and warning events.) 


##### - Level.FAXLOG_LEVEL_MIN

The fax server logs only the most severe failure events.


##### - Level.FAXLOG_LEVEL_NONE

The fax server does not log events.


## -remarks



The fax client application passes the <b>FAX_LOG_CATEGORY</b> structure in a call to the <a href="https://msdn.microsoft.com/4faddf91-a689-4247-86af-8d6dbc1b6af3">FaxSetLoggingCategories</a> function to modify the current logging categories for the fax server of interest. If the application calls the <a href="https://msdn.microsoft.com/bcd650b3-92f3-4b3b-b4c2-c3418f914711">FaxGetLoggingCategories</a> function, it returns the current settings in a <b>FAX_LOG_CATEGORY</b> structure. For more information, see <a href="https://msdn.microsoft.com/958fecf7-a787-4f86-bc67-53f7564ec43a">Managing Logging Categories</a>.




## -see-also




<a href="https://msdn.microsoft.com/be81e221-4aba-4c63-9640-337bee49fdb4">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/bcd650b3-92f3-4b3b-b4c2-c3418f914711">FaxGetLoggingCategories</a>



<a href="https://msdn.microsoft.com/4faddf91-a689-4247-86af-8d6dbc1b6af3">FaxSetLoggingCategories</a>
 

 

