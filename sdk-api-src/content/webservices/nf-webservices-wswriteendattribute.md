---
UID: NF:webservices.WsWriteEndAttribute
title: WsWriteEndAttribute function (webservices.h)
author: windows-sdk-content
description: This operation finishes writing an attribute to the current element. If WsWriteStartAttribute is called the Writer does not permit another element or attribute to be written until WsWriteEndAttribute is called.
old-location: wsw\wswriteendattribute.htm
tech.root: wsw
ms.assetid: 8747c484-19b3-46b2-beee-80b220011def
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsWriteEndAttribute, WsWriteEndAttribute function [Web Services for Windows], webservices/WsWriteEndAttribute, wsw.wswriteendattribute
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
 - WsWriteEndAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsWriteEndAttribute function


## -description


This operation finishes writing an attribute to the current element.
      If <a href="https://msdn.microsoft.com/9fd1eed9-6d8b-4b2e-a7ad-54a7f584734f">WsWriteStartAttribute</a> is called the Writer does not permit another element
        or attribute to be written until <b>WsWriteEndAttribute</b> is called.
      


## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the attribute is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation is not allowed due to the current state of the object.

</td>
</tr>
</table>
 



