---
UID: NF:icontact.IContactCollection.Reset
title: IContactCollection::Reset
author: windows-sdk-content
description: Resets the enumerator to before the logical first element.
old-location: wincontacts\_wincontacts_IContactCollection_Reset.htm
tech.root: wincontacts
ms.assetid: 31922d03-079e-4a6f-8516-d4cf540d812e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IContactCollection interface [Windows Contacts],Reset method, IContactCollection.Reset, IContactCollection::Reset, Reset, Reset method [Windows Contacts], Reset method [Windows Contacts],IContactCollection interface, _wincontacts_IContactCollection_Reset, icontact/IContactCollection::Reset, wincontacts._wincontacts_IContactCollection_Reset
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
 - IContactCollection.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContactCollection::Reset


## -description


Resets the enumerator to before the logical first element.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A call to <a href="https://msdn.microsoft.com/e5a5d27d-121a-4755-892e-53d148facd74">IContactCollection::GetCurrent</a> immediately after <b>IContactCollection::Reset</b> is undefined. To get the first contact, call <a href="https://msdn.microsoft.com/f7d47643-4ef2-41fb-9f75-2fe79fec2385">IContactCollection::Next</a> first to ensure that there is one. 



