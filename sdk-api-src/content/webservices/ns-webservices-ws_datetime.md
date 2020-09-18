---
UID: NS:webservices._WS_DATETIME
title: WS_DATETIME (webservices.h)
description: This structure is used to represent dates and times.
helpviewer_keywords: ["WS_DATETIME","WS_DATETIME structure [Web Services for Windows]","webservices/WS_DATETIME","wsw.ws_datetime"]
old-location: wsw\ws_datetime.htm
tech.root: wsw
ms.assetid: 635f8e0b-f994-4500-85ad-dd74fb4a6c22
ms.date: 12/05/2018
ms.keywords: WS_DATETIME, WS_DATETIME structure [Web Services for Windows], webservices/WS_DATETIME, wsw.ws_datetime
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: WS_DATETIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DATETIME
 - webservices/_WS_DATETIME
 - WS_DATETIME
 - webservices/WS_DATETIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_DATETIME
---

# WS_DATETIME structure


## -description

This structure is used to represent dates and times.
      

Represents dates and times with values ranging from 12:00:00 midnight, 
        January 1, 0001 Anno Domini (Common Era) through 11:59:59 P.M., 
        December 31, 9999 A.D. (C.E.) to an accuracy of 100 nanoseconds.
      

The functions <a href="/windows/desktop/api/webservices/nf-webservices-wsdatetimetofiletime">WsDateTimeToFileTime</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsfiletimetodatetime">WsFileTimeToDateTime</a> 
        can be used to convert a <b>WS_DATETIME</b> to and from a FILETIME.

## -struct-fields

### -field ticks

The time in 100 nanosecond units, with 0 representing 12:00:00 midnight January 1, Anno Domini (Common Era).  The
          largest representable value is 3155378975999999999, which corresponds to 100 nanoseconds prior to 12:00:00 midnight
          January 1, 10000.

### -field format

The format that is used when representing this time as text.