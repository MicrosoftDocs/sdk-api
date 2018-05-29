---
UID: NF:webservices.WsFileTimeToDateTime
title: WsFileTimeToDateTime function
author: windows-sdk-content
description: Takes a reference to a FILETIME object and converts it into a WS_DATETIME object. A reference to the WS_DATETIME object is returned by output parameter.
old-location: wsw\wsfiletimetodatetime.htm
old-project: wsw
ms.assetid: 75a547f8-c8dc-47c3-97c9-2a39b046263f
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsFileTimeToDateTime, WsFileTimeToDateTime function [Web Services for Windows], webservices/WsFileTimeToDateTime, wsw.wsfiletimetodatetime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsFileTimeToDateTime
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsFileTimeToDateTime function


## -description


Takes a reference to a FILETIME object and converts it into a <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> object.
       A reference to the WS_DATETIME object is returned by output parameter.


## -parameters




### -param fileTime [in]


          A pointer to the FILETIME structure to convert.
        


### -param dateTime [out]


          A pointer to the new WS_DATETIME object that has the newly converted time.
        


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>
 




## -remarks




        A <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> cannot represent dates from the year 10000 and beyond.  A FILETIME representing a date
        later than this will cause the function return <b>WS_E_INVALID_FORMAT</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


        The format field of the <a href="https://msdn.microsoft.com/635f8e0b-f994-4500-85ad-dd74fb4a6c22">WS_DATETIME</a> will be set to <a href="https://msdn.microsoft.com/e5859797-90dd-4509-ae41-f8d8c83cfd9c">WS_DATETIME_FORMAT_UTC</a>.
      



