---
UID: NN:winsync.IRecoverableErrorData
title: IRecoverableErrorData (winsync.h)
author: windows-sdk-content
description: Represents information about a recoverable error.
old-location: winsync\irecoverableerrordata.htm
tech.root: winsync
ms.assetid: e99779ef-87c9-45ac-93dc-53ee1a201402
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRecoverableErrorData, IRecoverableErrorData interface [Windows Sync], IRecoverableErrorData interface [Windows Sync],described, winsync.irecoverableerrordata, winsync/IRecoverableErrorData
ms.topic: interface
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
 - IRecoverableErrorData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRecoverableErrorData interface


## -description


Represents information about a recoverable error.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRecoverableErrorData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRecoverableErrorData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRecoverableErrorData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bd268aa-683d-4a77-966c-7cba0348d034">GetErrorDescription</a>
</td>
<td align="left" width="63%">
Gets the description of the error.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b40d528-18dc-4924-959a-cde5f02d18b1">GetItemDisplayName</a>
</td>
<td align="left" width="63%">
Gets the display name of the item that caused the error.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df34b3ee-fc78-47ca-8916-ee4a81110628">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object by using the specified display name of the item that caused the error and a description of the error.


</td>
</tr>
</table> 


## -remarks



To communicate additional information that is not supported by this interface, implement an object that inherits from <b>IRecoverableErrorData</b> and also from a custom interface. When the application receives the <b>IRecoverableErrorData</b> object in the <a href="https://msdn.microsoft.com/de496e83-cfa4-47c7-9b07-712e59737532">ISyncCallback::OnRecoverableError</a> method, the application can call <b>QueryInterface</b> on the <b>IRecoverableErrorData</b> object to obtain the custom interface.




## -see-also




<a href="https://msdn.microsoft.com/de496e83-cfa4-47c7-9b07-712e59737532">ISyncCallback::OnRecoverableError Method</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

