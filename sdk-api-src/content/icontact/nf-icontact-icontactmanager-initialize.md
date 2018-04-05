---
UID: NF:icontact.IContactManager.Initialize
title: IContactManager::Initialize method
author: windows-driver-content
description: Initializes the contact manager with the unique application name and application version being used to manipulate contacts.
old-location: wincontacts\_wincontacts_IContactManager_Initialize.htm
old-project: wincontacts
ms.assetid: 50e87ba0-fcf0-4b64-87f4-dfb0ff16373f
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IContactManager, IContactManager interface [Windows Contacts], Initialize method, IContactManager::Initialize, Initialize method [Windows Contacts], Initialize method [Windows Contacts], IContactManager interface, Initialize,IContactManager.Initialize, _wincontacts_IContactManager_Initialize, icontact/IContactManager::Initialize, wincontacts._wincontacts_IContactManager_Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: COLORMATCHSETUPW, *PCOLORMATCHSETUPW, *LPCOLORMATCHSETUPW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wab32.dll
api_name:
-	IContactManager.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactManager::Initialize method


## -description


Initializes the contact manager with the unique application name and application version 
		being used to manipulate contacts.


## -parameters




### -param pszAppName [in]

Type: <b>LPWSTR</b>

Specifies the application name.


### -param pszAppVersion [in]

Type: <b>LPCWSTR</b>

Specifies the application version. 


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

<a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a> is initialized. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This method MUST be called before other <a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a> methods.</div>
<div> </div>


