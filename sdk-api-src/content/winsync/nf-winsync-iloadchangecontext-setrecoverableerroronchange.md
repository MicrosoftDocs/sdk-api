---
UID: NF:winsync.ILoadChangeContext.SetRecoverableErrorOnChange
title: ILoadChangeContext::SetRecoverableErrorOnChange
author: windows-sdk-content
description: Indicates a recoverable error on this change has occurred.
old-location: winsync\iloadchangecontext_setrecoverableerroronchange.htm
tech.root: winsync
ms.assetid: 9e557889-a4f6-4e05-99ce-bb05013dc4cd
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ILoadChangeContext interface [Windows Sync],SetRecoverableErrorOnChange method, ILoadChangeContext.SetRecoverableErrorOnChange, ILoadChangeContext::SetRecoverableErrorOnChange, SetRecoverableErrorOnChange, SetRecoverableErrorOnChange method [Windows Sync], SetRecoverableErrorOnChange method [Windows Sync],ILoadChangeContext interface, winsync.iloadchangecontext_setrecoverableerroronchange, winsync/ILoadChangeContext::SetRecoverableErrorOnChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ILoadChangeContext.SetRecoverableErrorOnChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILoadChangeContext::SetRecoverableErrorOnChange


## -description


Indicates a recoverable error on this change has occurred.


## -parameters




### -param hrError [in]

The error code that is associated with the error that prevented the item data from being loaded.


### -param pErrorData [in]

Additional information about the error.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>hrError</i> does not specify an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
</table>
 




## -remarks



When this method is called, an <b>ISingleItemException</b> object is added to the learned knowledge; and the item change will not be enumerated again for the duration of the synchronization session.




## -see-also




<a href="https://msdn.microsoft.com/11d8971b-354f-4347-9d3f-6d32df8dc9d2">ILoadChangeContext Interface</a>



<a href="https://msdn.microsoft.com/623553cb-9dc2-4504-9c49-357a0526b130">ISingleItemException Interface</a>
 

 

