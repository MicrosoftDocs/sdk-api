---
UID: NF:webservices.WsReadStartAttribute
title: WsReadStartAttribute function (webservices.h)
author: windows-sdk-content
description: Moves the Reader to the specified attribute so that the content may be read using WsReadValue, WsReadChars, or WsReadBytes.
old-location: wsw\wsreadstartattribute.htm
tech.root: wsw
ms.assetid: 6fd0c8c2-2eac-4d98-898d-1c5849220c36
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsReadStartAttribute, WsReadStartAttribute function [Web Services for Windows], webservices/WsReadStartAttribute, wsw.wsreadstartattribute
ms.topic: function
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsReadStartAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsReadStartAttribute function


## -description


Moves the Reader to the specified attribute so that the content may be read using <a href="https://msdn.microsoft.com/d2dbeaf1-29cb-4848-8188-7922fdc15091">WsReadValue</a>, <a href="https://msdn.microsoft.com/3285d3f7-8ab1-42f0-b6e0-1d91aa0d576f">WsReadChars</a>, or <a href="https://msdn.microsoft.com/02cff29c-7d39-4df2-8eb1-506f93959a1e">WsReadBytes</a>.
      
        If the reader is not positioned on a start element then it returns a <b>WS_E_INVALID_FORMAT</b> exception.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)<div class="alert"><b>Note</b>  Attributes read do not appear in any particular order.  <a href="https://msdn.microsoft.com/beb00382-6cc0-42c6-b835-4ebc94c5faa2">WsFindAttribute</a> can
        be used to locate the index of a particular attribute.
      </div>
<div> </div>



## -parameters




### -param reader [in]

A pointer to the <b>XML Reader</b> object used to read the Start attribute.
          


### -param attributeIndex [in]

The index of the attribute to read.
        


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
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a> function returns EOF when advanced within an attribute.  The <a href="https://msdn.microsoft.com/1181ca68-f67b-47e1-b9de-1bc57ecf36f6">WsReadEndAttribute</a> function can be used
        to return the reader to the containing element.
      



