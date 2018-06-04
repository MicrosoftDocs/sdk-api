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

# IWMSInternalAdminNetSource::GetCredentialFlags


## -description



The <b>GetCredentialFlags</b> method can be used in conjunction with <a href="https://msdn.microsoft.com/af6208b3-84f6-44d1-9587-140044f2b2f0">IWMSInternalAdminNetSource::SetCredentialFlags</a> to determine whether the user wants passwords saved as a default behavior. This method retrieves any flags previously set.




## -parameters




### -param lpdwFlags [out]

<b>DWORD</b> containing credential flags. At this time, the only supported flag is 0x1, which signifies that the user has stated a preference that passwords should be saved automatically.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/e4d6bcc3-a32b-4270-8b43-f3b6a5046fd6">IWMSInternalAdminNetSource::GetCredentials</a>



<a href="https://msdn.microsoft.com/af6208b3-84f6-44d1-9587-140044f2b2f0">IWMSInternalAdminNetSource::SetCredentialFlags</a>
 

 

