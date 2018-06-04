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

# ICredentialProviderCredential::SetSelected


## -description


Called when a credential is selected. Enables the implementer to set logon characteristics.


## -parameters




### -param pbAutoLogon [out]

Type: <b>BOOL*</b>

When this method returns, contains <b>TRUE</b> if selection of the credential indicates that it should attempt to logon immediately and automatically, otherwise <b>FALSE</b>. For example, a credential provider that enumerates an account without a password may want to return this as true.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Returning any value other than <b>S_OK</b> causes the Logon UI and Credential UI to behave as if no selection occurred.

In Windows 10, if a credential provider wants to automatically log the user on in a situation Windows does not think is appropriate, the system will display a sign in button as a speed bump. One example of this is when a user with an empty password locks the computer or signs out. In that scenario,  Windows does not directly log the user back in. 




