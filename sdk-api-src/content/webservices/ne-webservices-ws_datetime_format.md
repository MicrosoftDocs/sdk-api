---
UID: NE:webservices.WS_DATETIME_FORMAT
title: WS_DATETIME_FORMAT
author: windows-sdk-content
description: Specifies the textual format of a WS_DATETIME.
old-location: wsw\ws_datetime_format.htm
old-project: wsw
ms.assetid: e5859797-90dd-4509-ae41-f8d8c83cfd9c
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_DATETIME_FORMAT, WS_DATETIME_FORMAT enumeration [Web Services for Windows], WS_DATETIME_FORMAT_LOCAL, WS_DATETIME_FORMAT_NONE, WS_DATETIME_FORMAT_UTC, webservices/WS_DATETIME_FORMAT, webservices/WS_DATETIME_FORMAT_LOCAL, webservices/WS_DATETIME_FORMAT_NONE, webservices/WS_DATETIME_FORMAT_UTC, wsw.ws_datetime_format
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_DATETIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_DATETIME_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_DATETIME_FORMAT enumeration


## -description



        Specifies the textual format of a <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a>.
      


## -enum-fields




### -field WS_DATETIME_FORMAT_UTC


          This format displays a time in the GMT timezone.  It is formatted with a "Z" following the time.
          For example, September 25, 2007 at 1:30AM in the GMT timezone would be represented as "2007-09-25T01:30:00Z".
        


### -field WS_DATETIME_FORMAT_LOCAL


          This format displays a time with a specific timezone.  The time is followed by "[+|-]hh:mm" indicating the
          relative difference between the local time and UTC in hours and minutes.
          For example, September 27, 2007 at 10:30AM in the Pacific timezone would be represented as
          "2007-09-27T10:30:00-07:00".
        


          If the system is unable to convert the time to a local format because timezone information for the time
          specified it not available, then it will format the time as <a href="https://msdn.microsoft.com/e5859797-90dd-4509-ae41-f8d8c83cfd9c">WS_DATETIME_FORMAT_UTC</a>.
        


### -field WS_DATETIME_FORMAT_NONE


          This format displays a time with no timezone.  The time is formatted with no additional information and no
          timezone is implied.  For example, September 27, 2007 at 10:30AM would be represented as "2007-09-27T10:30:00".
        

