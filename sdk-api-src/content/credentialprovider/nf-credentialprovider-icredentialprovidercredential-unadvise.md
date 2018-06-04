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

# ICredentialProviderCredential::UnAdvise


## -description


Used by the Logon UI or Credential UI to advise the credential that event callbacks are no longer accepted.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is optional. If you do not implement this method, you should just return <b>E_NOTIMPL</b>.

If this method is called, it indicates that the <a href="https://msdn.microsoft.com/258449a4-78e2-475e-ab16-6481207e7354">ICredentialProviderCredentialEvents</a> pointer provided in <a href="https://msdn.microsoft.com/26db5ec5-78bf-4d88-90af-c822c8d3ce45">Advise</a> is no longer valid. It is the responsibility of the credential provider to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on the provided <b>ICredentialProviderCredentialEvents</b> pointer during this method.




## -see-also




<a href="https://msdn.microsoft.com/ef9bb148-0b4e-4c13-b69d-3e63a5592e4a">ICredentialProviderCredential</a>



<a href="https://msdn.microsoft.com/26db5ec5-78bf-4d88-90af-c822c8d3ce45">ICredentialProviderCredential::Advise</a>
 

 

