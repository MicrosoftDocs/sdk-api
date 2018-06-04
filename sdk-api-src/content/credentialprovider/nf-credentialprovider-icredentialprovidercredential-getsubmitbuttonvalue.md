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

# ICredentialProviderCredential::GetSubmitButtonValue


## -description


Retrieves the identifier of a field that the submit button should be placed next to in the Logon UI. The Credential UI does not call this method.


## -parameters




### -param dwFieldID [in]

Type: <b>DWORD</b>

The identifier for the field a submit button value is needed for.


### -param pdwAdjacentTo [out]

Type: <b>DWORD*</b>

A pointer to a value that receives the field ID of the field that the submit button should be placed next to.

<b>Note to implementers:</b> Do not return the field ID of a bitmap in this parameter. It is not good UI design to place the submit button next to a bitmap, and doing so can cause a failure in the Logon UI.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The submit button is not labeled as such; that is simply a generic way to refer to the button you click to submit the credentials. The button normally appears as a circular button that contains an arrow pointing to the right, although this appearance could change in later releases. For more information, see <a href="https://msdn.microsoft.com/5af9f007-9588-4574-a5ce-3f01ec0b45e8">CPFT_SUBMIT_BUTTON</a>.

You should not hide the submit button unless your credential provider always performs automatic submission. Otherwise it can be confusing to the users since they will not see a way to submit their credentials.

Call this method when assembling the Logon UI. For example usage, see the Credential Providers samples included in the Windows Software Development Kit (SDK).

.



