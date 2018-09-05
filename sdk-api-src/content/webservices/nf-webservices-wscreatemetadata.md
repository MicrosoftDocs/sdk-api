---
UID: NF:webservices.WsCreateMetadata
title: WsCreateMetadata function
author: windows-sdk-content
description: Creates a metadata object that is used to collect and process metadata documents.
old-location: wsw\wscreatemetadata.htm
old-project: wsw
ms.assetid: c3b6f926-331b-46a7-8180-36762abf63d7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WsCreateMetadata, WsCreateMetadata function [Web Services for Windows], webservices/WsCreateMetadata, wsw.wscreatemetadata
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
 - WsCreateMetadata
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateMetadata function


## -description



Creates a metadata object that is used to collect and process metadata documents.




## -parameters




### -param properties

An array of <a href="https://msdn.microsoft.com/72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4">WS_METADATA_PROPERTY</a> structures containing optional properties for the metadata.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param metadata

On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/aa7383a1-60fa-448a-b0c6-b9c49d9d5070">WS_METADATA</a> structure representing the new message.
                
                When you no longer need this structure, you must free it by calling <a href="https://msdn.microsoft.com/4e159619-3807-4e7f-9198-fb74962ae141">WsFreeMetadata</a>.


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 



