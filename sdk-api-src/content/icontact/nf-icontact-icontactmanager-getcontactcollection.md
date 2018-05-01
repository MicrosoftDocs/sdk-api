---
UID: NF:icontact.IContactManager.GetContactCollection
title: IContactManager::GetContactCollection method
author: windows-driver-content
description: Returns an IContactCollection object that contains all known contacts.
old-location: wincontacts\_wincontacts_IContactManager_GetContactCollection.htm
old-project: wincontacts
ms.assetid: 6b9d7ba5-e2cd-452f-8479-fdaad183b1ac
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetContactCollection method [Windows Contacts], GetContactCollection method [Windows Contacts], IContactManager interface, GetContactCollection,IContactManager.GetContactCollection, IContactManager, IContactManager interface [Windows Contacts], GetContactCollection method, IContactManager::GetContactCollection, _wincontacts_IContactManager_GetContactCollection, icontact/IContactManager::GetContactCollection, wincontacts._wincontacts_IContactManager_GetContactCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: icontact.h
req.include-header: 
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
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wab32.dll
api_name:
-	IContactManager.GetContactCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactManager::GetContactCollection method


## -description


Returns an <a href="https://msdn.microsoft.com/4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897">IContactCollection</a> object that contains all known contacts. 


## -parameters




### -param ppContactCollection [out]

Type: <b><a href="https://msdn.microsoft.com/4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897">IContactCollection</a>**</b>

On success, contains an enumeration of the contact collection. 


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
Success. <i>ppContactCollection</i> contains the collection. 

</td>
</tr>
</table>
 




## -remarks



The enumerator of the new collection is set before the first contact. You must first call <a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a> before querying the collection with <a href="https://msdn.microsoft.com/e5a5d27d-121a-4755-892e-53d148facd74">GetCurrent</a>.



