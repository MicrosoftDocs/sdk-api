---
UID: NF:webservices.WsResetError
title: WsResetError function (webservices.h)
author: windows-sdk-content
description: Releases the content of the error object parameter but does not release the resource allocated to the error object parameter.
old-location: wsw\wsreseterror.htm
tech.root: wsw
ms.assetid: a01a65f1-3eca-452c-a10d-dc9c6c3db124
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WsResetError, WsResetError function [Web Services for Windows], webservices/WsResetError, wsw.wsreseterror
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
 - WsResetError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsResetError function


## -description


Releases the content of the <i>error</i> object parameter but does not release the resource allocated to the <i>error</i> object parameter. 
            <div class="alert"><b>Note</b>  The "reset" effect of this function returns the <i>error</i> object to the state set at instantiation. The object is not released consequently is available for reuse.
            </div>
<div> </div>



## -parameters




### -param error [in]

This parameter is a   pointer to the <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object to reset.


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
</table>
 




## -remarks





String data added to the error object using the <a href="https://msdn.microsoft.com/5fdad296-5024-4360-b1c5-f0192929c612">WsAddErrorString</a> function are released.
            

Properties that have been set using the  <a href="https://msdn.microsoft.com/5193eaf4-29f7-4e97-a3b0-97441b26399c">WsSetErrorProperty</a> function are released.
            



