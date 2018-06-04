---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICredentialProviderCredential::GetComboBoxValueCount


## -description


Gets a count of the items in the specified combo box and designates which item should have initial selection.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the combo box to gather information about.


### -param pcItems [out]

Type: <b>DWORD*</b>

A pointer to the number of items in the given combo box.


### -param pdwSelectedItem [out]

Type: <b>DWORD*</b>

Contains a pointer to the item that receives initial selection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Credential UI and Logon UI use this method to obtain the number of items in a combo box and designate which item should have initial selection.



