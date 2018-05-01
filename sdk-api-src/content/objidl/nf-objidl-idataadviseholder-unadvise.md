---
UID: NF:objidl.IDataAdviseHolder.Unadvise
title: IDataAdviseHolder::Unadvise method
author: windows-driver-content
description: Removes a connection between a data object and an advisory sink that was set up through a previous call to IDataAdviseHolder::Advise. This method is typically called in the implementation of IDataObject::DUnadvise.
old-location: com\idataadviseholder_unadvise.htm
old-project: com
ms.assetid: baeb29fd-1dd2-4320-911d-b271b2250184
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IDataAdviseHolder, IDataAdviseHolder interface [COM], Unadvise method, IDataAdviseHolder::Unadvise, Unadvise method [COM], Unadvise method [COM], IDataAdviseHolder interface, Unadvise,IDataAdviseHolder.Unadvise, _ole_idataadviseholder_unadvise, com.idataadviseholder_unadvise, objidl/IDataAdviseHolder::Unadvise
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IDataAdviseHolder.Unadvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataAdviseHolder::Unadvise method


## -description


Removes a connection between a data object and an advisory sink that was set up through a previous call to <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a>. This method is typically called in the implementation of <a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a>.


## -parameters




### -param dwConnection [in]

A token that specifies the connection to be removed. This value was returned by <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a> when the connection was originally established.


## -returns



This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwConnection</i> parameter does not specify a valid connection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/bb9ae4c5-8655-4553-9a1c-ce52c6c86299">IDataObject::DUnadvise</a>
 

 

