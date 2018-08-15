---
UID: NF:webservices.WsWriteStartCData
title: WsWriteStartCData function
author: windows-sdk-content
description: This operation starts a CDATA section in the writer.
old-location: wsw\wswritestartcdata.htm
old-project: wsw
ms.assetid: c233244c-24b6-4baa-ba36-697283ff33f3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsWriteStartCData, WsWriteStartCData function [Web Services for Windows], webservices/WsWriteStartCData, wsw.wswritestartcdata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.redist: 
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
 - WsWriteStartCData
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsWriteStartCData function


## -description


This operation starts a CDATA section in the writer.
      CDATA sections cannot be nested and cannot appear at the root of the document.  <div class="alert"><b>Note</b>  Some encodings do not support CDATA
        and will generate text instead.
      </div>
<div> </div>The CDATA section is completed by calling <a href="https://msdn.microsoft.com/7b8c27b8-4540-4d47-9622-904428233d30">WsWriteEndCData</a>.
      


## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the CDATA section is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


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
 



