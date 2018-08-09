---
UID: NF:icontact.IContactPropertyCollection.Next
title: IContactPropertyCollection::Next
author: windows-sdk-content
description: Moves to the next property.
old-location: wincontacts\_wincontacts_IContactPropertyCollection_Next.htm
old-project: wincontacts
ms.assetid: b6e8abad-796d-4ded-be23-45ca107915f1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IContactPropertyCollection interface [Windows Contacts],Next method, IContactPropertyCollection.Next, IContactPropertyCollection::Next, Next, Next method [Windows Contacts], Next method [Windows Contacts],IContactPropertyCollection interface, _wincontacts_IContactPropertyCollection_Next, icontact/IContactPropertyCollection::Next, wincontacts._wincontacts_IContactPropertyCollection_Next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: icontact.h
req.include-header: Contact.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Icontact.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactPropertyCollection.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactPropertyCollection::Next


## -description


Moves to the next property.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

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
Move is successful. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not move, positioned at the end of the collection. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  After S_FALSE, further calls to interface's query methods will fail.</div>
<div> </div>


