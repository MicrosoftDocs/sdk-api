---
UID: NF:icontact.IContactPropertyCollection.Reset
title: IContactPropertyCollection::Reset
author: windows-sdk-content
description: Resets enumeration of properties.
old-location: wincontacts\_wincontacts_IContactPropertyCollection_Reset.htm
old-project: wincontacts
ms.assetid: cef73e3c-56be-44b8-b05b-3c2081b71591
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IContactPropertyCollection interface [Windows Contacts],Reset method, IContactPropertyCollection.Reset, IContactPropertyCollection::Reset, Reset, Reset method [Windows Contacts], Reset method [Windows Contacts],IContactPropertyCollection interface, _wincontacts_IContactPropertyCollection_Reset, icontact/IContactPropertyCollection::Reset, wincontacts._wincontacts_IContactPropertyCollection_Reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: icontact.h
req.include-header: Contact.h
req.redist: 
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
 - IContactPropertyCollection.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactPropertyCollection::Reset


## -description


Resets enumeration of properties.


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
Reset is successful. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Collection has been reset to the location before the first element (if any elements are present), 
		so you must call <a href="https://msdn.microsoft.com/b6e8abad-796d-4ded-be23-45ca107915f1">IContactPropertyCollection::Next</a> to begin querying data.</div>
<div> </div>


