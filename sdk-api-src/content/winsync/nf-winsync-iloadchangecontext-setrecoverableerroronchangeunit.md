---
UID: NF:winsync.ILoadChangeContext.SetRecoverableErrorOnChangeUnit
title: ILoadChangeContext::SetRecoverableErrorOnChangeUnit
author: windows-sdk-content
description: Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.
old-location: winsync\iloadchangecontext_setrecoverableerroronchangeunit.htm
tech.root: winsync
ms.assetid: 0489a26c-5760-4e41-84c9-45868d27b67c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ILoadChangeContext interface [Windows Sync],SetRecoverableErrorOnChangeUnit method, ILoadChangeContext.SetRecoverableErrorOnChangeUnit, ILoadChangeContext::SetRecoverableErrorOnChangeUnit, SetRecoverableErrorOnChangeUnit, SetRecoverableErrorOnChangeUnit method [Windows Sync], SetRecoverableErrorOnChangeUnit method [Windows Sync],ILoadChangeContext interface, winsync.iloadchangecontext_setrecoverableerroronchangeunit, winsync/ILoadChangeContext::SetRecoverableErrorOnChangeUnit
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
 - ILoadChangeContext.SetRecoverableErrorOnChangeUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILoadChangeContext::SetRecoverableErrorOnChangeUnit


## -description


Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store.


## -parameters




### -param hrError [in]

The error code that is associated with the error that prevented the change unit data from being loaded.


### -param pChangeUnit [in]

The change unit change that caused the error.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_ON_CREATE_MUST_FAIL_ENTIRE_ITEM</b></dt>
</dl>
</td>
<td width="60%">
The change that contains this change unit refers to an item creation. In this case, the error must be reported on the item change by using <a href="https://msdn.microsoft.com/9e557889-a4f6-4e05-99ce-bb05013dc4cd">ILoadChangeContext::SetRecoverableErrorOnChange</a>.

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



When this method is called, an <b>IChangeUnitException</b> object is added to the learned knowledge; and the change unit change will not be enumerated again for the duration of the synchronization session.





## -see-also




<a href="https://msdn.microsoft.com/3b47abab-0a33-405f-a765-307ab800bad6">IChangeUnitException Interface</a>



<a href="https://msdn.microsoft.com/11d8971b-354f-4347-9d3f-6d32df8dc9d2">ILoadChangeContext Interface</a>
 

 

