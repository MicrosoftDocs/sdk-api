---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
            



