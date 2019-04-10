---
UID: NF:webservices.WsResetMetadata
title: WsResetMetadata function (webservices.h)
author: windows-sdk-content
description: Resets a metadata object state to WS_METADATA_STATE_CREATED. In this state the Metadata object can be reused. WS_POLICY objects that were retrieved using the Metadata object will be released.
old-location: wsw\wsresetmetadata.htm
tech.root: wsw
ms.assetid: 091a227a-62d4-4625-9e96-b03f96e2304a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsResetMetadata, WsResetMetadata function [Web Services for Windows], webservices/WsResetMetadata, wsw.wsresetmetadata
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
 - WsResetMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsResetMetadata function


## -description


Resets a metadata object state to <b>WS_METADATA_STATE_CREATED</b>.
            
                In this state the Metadata object can be reused.
            <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> objects that
                were retrieved using the Metadata object will be released.
            




## -parameters




### -param metadata [in]

A pointer to the <b>Metadata</b> object to reset.  The pointer must reference a valid <a href="https://msdn.microsoft.com/aa7383a1-60fa-448a-b0c6-b9c49d9d5070">WS_METADATA</a>.
                


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
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The metadata was in an inappropriate state.
                

</td>
</tr>
</table>
 




## -remarks



Reusing a metadata instead of creating one from scratch may improve performance.
            If called correctly, this function will not fail.
            



