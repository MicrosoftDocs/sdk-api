---
UID: NF:winsync.IChangeConflict.GetDestinationProviderConflictingData
title: IChangeConflict::GetDestinationProviderConflictingData (winsync.h)
author: windows-sdk-content
description: Gets an object that can be used to retrieve item data for the change item from the destination replica.
old-location: winsync\ichangeconflict_getdestinationproviderconflictingdata.htm
tech.root: winsync
ms.assetid: 7a63d554-56e0-4c39-94ea-613fecc97331
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDestinationProviderConflictingData, GetDestinationProviderConflictingData method [Windows Sync], GetDestinationProviderConflictingData method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetDestinationProviderConflictingData method, IChangeConflict.GetDestinationProviderConflictingData, IChangeConflict::GetDestinationProviderConflictingData, winsync.ichangeconflict_getdestinationproviderconflictingdata, winsync/IChangeConflict::GetDestinationProviderConflictingData
ms.topic: method
f1_keywords: ["winsync/IChangeConflict.GetDestinationProviderConflictingData"]
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
 - IChangeConflict.GetDestinationProviderConflictingData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IChangeConflict::GetDestinationProviderConflictingData


## -description


Gets an object that can be used to retrieve item data for the change item from the destination replica.


## -parameters




### -param ppConflictingData [out]

Returns an object that can be used to retrieve item data for the change item from the destination replica.


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
<dt><b>SYNC_E_INTERNAL_ERROR </b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Provider-specified error codes.</b></dt>
</dl>
</td>
<td width="60%">
The provider cannot load the data for the change.

</td>
</tr>
</table>
 




## -remarks



The object that is returned in <i>ppConflictingData</i> can be an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever</a> object or a provider-specific object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever Interface</a>
 

 

