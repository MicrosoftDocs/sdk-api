---
UID: NE:webservices.__unnamed_enum_102
title: WS_DATETIME_FORMAT (webservices.h)
description: Specifies the textual format of a WS_DATETIME.
helpviewer_keywords: ["WS_DATETIME_FORMAT","WS_DATETIME_FORMAT enumeration [Web Services for Windows]","WS_DATETIME_FORMAT_LOCAL","WS_DATETIME_FORMAT_NONE","WS_DATETIME_FORMAT_UTC","webservices/WS_DATETIME_FORMAT","webservices/WS_DATETIME_FORMAT_LOCAL","webservices/WS_DATETIME_FORMAT_NONE","webservices/WS_DATETIME_FORMAT_UTC","wsw.ws_datetime_format"]
old-location: wsw\ws_datetime_format.htm
tech.root: wsw
ms.assetid: e5859797-90dd-4509-ae41-f8d8c83cfd9c
ms.date: 12/05/2018
ms.keywords: WS_DATETIME_FORMAT, WS_DATETIME_FORMAT enumeration [Web Services for Windows], WS_DATETIME_FORMAT_LOCAL, WS_DATETIME_FORMAT_NONE, WS_DATETIME_FORMAT_UTC, webservices/WS_DATETIME_FORMAT, webservices/WS_DATETIME_FORMAT_LOCAL, webservices/WS_DATETIME_FORMAT_NONE, webservices/WS_DATETIME_FORMAT_UTC, wsw.ws_datetime_format
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
req.typenames: WS_DATETIME_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_DATETIME_FORMAT
 - webservices/WS_DATETIME_FORMAT
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
 - WS_DATETIME_FORMAT
---

# WS_DATETIME_FORMAT enumeration


## -description

Specifies the textual format of a <a href="/windows/desktop/api/webservices/ns-webservices-ws_datetime">WS_DATETIME</a>.

## -enum-fields

### -field WS_DATETIME_FORMAT_UTC:0

This format displays a time in the GMT timezone.  It is formatted with a "Z" following the time.
          For example, September 25, 2007 at 1:30AM in the GMT timezone would be represented as "2007-09-25T01:30:00Z".

### -field WS_DATETIME_FORMAT_LOCAL:1

This format displays a time with a specific timezone.  The time is followed by "[+\|-]hh:mm" indicating the
          relative difference between the local time and UTC in hours and minutes.
          For example, September 27, 2007 at 10:30AM in the Pacific timezone would be represented as
          "2007-09-27T10:30:00-07:00".
        

If the system is unable to convert the time to a local format because timezone information for the time
          specified it not available, then it will format the time as <a href="/windows/desktop/api/webservices/ne-webservices-ws_datetime_format">WS_DATETIME_FORMAT_UTC</a>.

### -field WS_DATETIME_FORMAT_NONE:2

This format displays a time with no timezone.  The time is formatted with no additional information and no
          timezone is implied.  For example, September 27, 2007 at 10:30AM would be represented as "2007-09-27T10:30:00".
