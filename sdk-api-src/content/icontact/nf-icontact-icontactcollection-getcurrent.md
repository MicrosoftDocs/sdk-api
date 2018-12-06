---
UID: NF:icontact.IContactCollection.GetCurrent
title: IContactCollection::GetCurrent
author: windows-sdk-content
description: Retrieves the current contact in the enumeration.
old-location: wincontacts\_wincontacts_IContactCollection_GetCurrent.htm
tech.root: wincontacts
ms.assetid: e5a5d27d-121a-4755-892e-53d148facd74
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrent, GetCurrent method [Windows Contacts], GetCurrent method [Windows Contacts],IContactCollection interface, IContactCollection interface [Windows Contacts],GetCurrent method, IContactCollection.GetCurrent, IContactCollection::GetCurrent, _wincontacts_IContactCollection_GetCurrent, icontact/IContactCollection::GetCurrent, wincontacts._wincontacts_IContactCollection_GetCurrent
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
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactCollection.GetCurrent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContactCollection::GetCurrent


## -description


Retrieves the current contact in the enumeration. 


## -parameters




### -param ppContact [out]

Type: <b><a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a>**</b>

If successful, contains the current contact. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After reset, a call to <b>IContactCollection::GetCurrent</b> without first calling <a href="https://msdn.microsoft.com/f7d47643-4ef2-41fb-9f75-2fe79fec2385">IContactCollection::Next</a> will fail. 




## -see-also




<a href="https://msdn.microsoft.com/4d7f26b0-a2c0-4c7b-8f1d-f918cb1e0897">IContactCollection</a>



<a href="https://msdn.microsoft.com/31922d03-079e-4a6f-8516-d4cf540d812e">IContactCollection::Reset</a>
 

 

