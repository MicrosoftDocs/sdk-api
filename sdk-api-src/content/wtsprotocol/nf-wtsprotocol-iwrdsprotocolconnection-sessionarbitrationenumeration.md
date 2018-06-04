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

# IWRdsProtocolConnection::SessionArbitrationEnumeration


## -description


Called after arbitration to allow the protocol to specify the sessions to be reconnected. The protocol extension should return <b>E_NOTIMPL</b> to use the default session arbitration.


## -parameters




### -param hUserToken [in]

A handle that represents the user token.


### -param bSingleSessionPerUserEnabled [in]

Specifies whether a user can only be associated with a single session.


### -param pSessionIdArray [out]

A pointer to a <b>ULONG</b> array that receives the disconnected session identifiers for the user. If this parameter is <b>NULL</b>, the Remote Desktop Services service is requesting the number of elements to allocate this array. Place the number of identifiers in the value pointed to by <i>pdwSessionIdentifierCount</i>.


### -param pdwSessionIdentifierCount [in, out]

A pointer to a <b>ULONG</b> value that receives the number of elements in the <i>pSessionIdArray</i> array.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>
 

 

