---
UID: NF:webservices.WsReadStartElement
title: WsReadStartElement function
author: windows-driver-content
description: Calling this function advances the reader past a start element skipping any whitespace.
old-location: wsw\wsreadstartelement.htm
old-project: wsw
ms.assetid: 88661ae5-2112-4a41-8fcd-03c74f6ec170
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WsReadStartElement, WsReadStartElement function [Web Services for Windows], webservices/WsReadStartElement, wsw.wsreadstartelement
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	WsReadStartElement
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadStartElement function


## -description



        Calling this function advances the reader past a start element skipping any whitespace.
      
        After parsing if the Reader is not positioned on a start element it will return a<b>WS_E_INVALID_FORMAT</b> exception.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


## -parameters




### -param reader [in]

A pointer to the <b>XML Reader</b> object used to read the Start element.
          


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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">

A quota was exceeded.

</td>
</tr>
</table>
 




## -remarks




        This function can fail for any of the reasons listed in <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a>.
      



