---
UID: NS:winfax._FAX_LOG_CATEGORYW
title: FAX_LOG_CATEGORYW (winfax.h)

description: The FAX_LOG_CATEGORY structure describes one logging category.
old-location: fax\_mfax_fax_log_category_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1fn6.htm

ms.date: 12/05/2018
ms.keywords: "*PFAX_LOG_CATEGORYW, FAXLOG_CATEGORY_INBOUND, FAXLOG_CATEGORY_INIT, FAXLOG_CATEGORY_OUTBOUND, FAXLOG_CATEGORY_UNKNOWN, FAXLOG_LEVEL_MAX, FAXLOG_LEVEL_MED, FAXLOG_LEVEL_MIN, FAXLOG_LEVEL_NONE, FAX_LOG_CATEGORY, FAX_LOG_CATEGORY structure [Fax Service], FAX_LOG_CATEGORYA, FAX_LOG_CATEGORYW, PFAX_LOG_CATEGORY, PFAX_LOG_CATEGORY structure pointer [Fax Service], _mfax_fax_log_category_str, fax._mfax_fax_log_category_str, winfax/FAX_LOG_CATEGORY, winfax/FAX_LOG_CATEGORYA, winfax/FAX_LOG_CATEGORYW, winfax/PFAX_LOG_CATEGORY"
ms.topic: struct
f1_keywords: 
 - "winfax/FAX_LOG_CATEGORY"
dev_langs:
 - c++
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_LOG_CATEGORYW (Unicode) and FAX_LOG_CATEGORYA (ANSI)
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
 - Winfax.h
api_name:
 - FAX_LOG_CATEGORY
 - FAX_LOG_CATEGORYA
 - FAX_LOG_CATEGORYW
targetos: Windows
req.typenames: FAX_LOG_CATEGORYW, *PFAX_LOG_CATEGORYW
req.redist: 
ms.custom: 19H1
---

# FAX_LOG_CATEGORYW structure


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



The fax client application passes the <b>FAX_LOG_CATEGORY</b> structure in a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetloggingcategoriesa">FaxSetLoggingCategories</a> function to modify the current logging categories for the fax server of interest. If the application calls the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetloggingcategoriesa">FaxGetLoggingCategories</a> function, it returns the current settings in a <b>FAX_LOG_CATEGORY</b> structure. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-managing-logging-categories">Managing Logging Categories</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetloggingcategoriesa">FaxGetLoggingCategories</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetloggingcategoriesa">FaxSetLoggingCategories</a>
 

 

