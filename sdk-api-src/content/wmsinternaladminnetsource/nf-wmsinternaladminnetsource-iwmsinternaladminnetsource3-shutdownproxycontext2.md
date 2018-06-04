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

# IWMSInternalAdminNetSource3::ShutdownProxyContext2


## -description



The <b>ShutdownProxyContext2</b> method releases the internal resources used by <a href="https://msdn.microsoft.com/03c52ed2-bf77-4013-89d6-544d048f1056">IWMSInternalAdminNetSource3::FindProxyForURLEx2</a>. To avoid memory leaks, you must call this method after you are finished making calls to <b>FindProxyForURLEx2</b>.




## -parameters




### -param qwProxyContext [in]

<b>QWORD</b> containing the proxy context. Set this to the last proxy context received from <b>FindProxyForURLEx2</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b4ca08a4-6e2d-4646-b101-67bac67300b1">IWMSInternalAdminNetSource3 Interface</a>
 

 

