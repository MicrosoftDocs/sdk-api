---
UID: NF:webservices.WsReadEndElement
title: WsReadEndElement function
author: windows-sdk-content
description: This function ensures that the current Reader node is an End element and advances the reader to the next node.
old-location: wsw\wsreadendelement.htm
old-project: wsw
ms.assetid: cd2e0e5a-9c73-4180-9c54-6742d87cb141
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsReadEndElement, WsReadEndElement function [Web Services for Windows], webservices/WsReadEndElement, wsw.wsreadendelement
ms.prod: windows
ms.technology: windows-sdk
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
 - WsReadEndElement
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsReadEndElement function


## -description



        This function ensures that the current Reader <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">node</a> is an <b>End element</b>
        and advances the reader to the next <b>node</b>.
      
        If the Reader is not positioned on an <b>End element</b> when the function is called it will skip whitespace attempting to find one.
        If after skipping whitespace it is not positioned on an <b>End element</b> it returns a <b>WS_E_INVALID_FORMAT</b> exception.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


## -parameters




### -param reader [in]


          
                    
                    A pointer to the <b>XML Reader</b> that is reads the <b>End element</b>.
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
      



