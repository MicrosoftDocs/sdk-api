---
UID: NF:webservices.WsReadEndAttribute
title: WsReadEndAttribute function
author: windows-sdk-content
description: Moves the reader back to the element node containing the attribute that was read.
old-location: wsw\wsreadendattribute.htm
old-project: wsw
ms.assetid: 1181ca68-f67b-47e1-b9de-1bc57ecf36f6
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsReadEndAttribute, WsReadEndAttribute function [Web Services for Windows], webservices/WsReadEndAttribute, wsw.wsreadendattribute
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
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsReadEndAttribute
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadEndAttribute function


## -description



        Moves the reader back to the element node containing the attribute that was read.
      


## -parameters




### -param reader [in]

A pointer to the <b>XML Reader</b> that reads the <b>End attribute</b>.
                  The pointer must reference a valid <a href="https://msdn.microsoft.com/7acbe407-e91b-435a-82bc-acbbc13cfcfd">WS_XML_READER</a> object.
        


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




<a href="https://msdn.microsoft.com/6fd0c8c2-2eac-4d98-898d-1c5849220c36">WsReadStartAttribute</a> must have been called in order to use this API.
      



