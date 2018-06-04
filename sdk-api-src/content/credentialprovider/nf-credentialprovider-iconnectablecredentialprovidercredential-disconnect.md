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

# IConnectableCredentialProviderCredential::Disconnect


## -description


Disconnects an <a href="https://msdn.microsoft.com/fe5f3145-b428-42c9-ab1d-1c0e63c4454b">IConnectableCredentialProviderCredential</a> object.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After a successful call to <a href="https://msdn.microsoft.com/0fe91d1a-811a-4956-bb2f-47712ae2a155">Connect</a>, the Logon UI displays a <b>Disconnect</b> button to the user. If the user clicks <b>Disconnect</b>, the Logon UI calls <b>Disconnect</b> on every credential provider that implements <a href="https://msdn.microsoft.com/fe5f3145-b428-42c9-ab1d-1c0e63c4454b">IConnectableCredentialProviderCredential</a>.



