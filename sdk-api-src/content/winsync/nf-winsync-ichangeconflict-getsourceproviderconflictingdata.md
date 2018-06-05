---
UID: NF:winsync.IChangeConflict.GetSourceProviderConflictingData
title: IChangeConflict::GetSourceProviderConflictingData
author: windows-sdk-content
description: Gets an object that can be used to retrieve item data for the change item from the source replica.
old-location: winsync\ichangeconflict_getsourceproviderconflictingdata.htm
old-project: winsync
ms.assetid: 4227b559-59e9-4b87-beb0-2d47f3d81414
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSourceProviderConflictingData, GetSourceProviderConflictingData method [Windows Sync], GetSourceProviderConflictingData method [Windows Sync],IChangeConflict interface, IChangeConflict interface [Windows Sync],GetSourceProviderConflictingData method, IChangeConflict.GetSourceProviderConflictingData, IChangeConflict::GetSourceProviderConflictingData, winsync.ichangeconflict_getsourceproviderconflictingdata, winsync/IChangeConflict::GetSourceProviderConflictingData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IChangeConflict.GetSourceProviderConflictingData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IChangeConflict::GetSourceProviderConflictingData


## -description


Gets an object that can be used to retrieve item data for the change item from the source replica.


## -parameters




### -param ppConflictingData [out]

Returns an object that can be used to retrieve item data for the change item from the source replica.


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



The object that is returned in <i>ppConflictingData</i> can be an <a href="https://msdn.microsoft.com/d59a5198-5878-4a48-b6c4-042afc36054d">ISynchronousDataRetriever</a> object or a provider-specific object.




## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>



<a href="https://msdn.microsoft.com/d59a5198-5878-4a48-b6c4-042afc36054d">ISynchronousDataRetriever Interface</a>
 

 

