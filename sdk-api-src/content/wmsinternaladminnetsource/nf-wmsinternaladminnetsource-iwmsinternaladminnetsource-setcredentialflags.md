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

# IWMSInternalAdminNetSource::SetCredentialFlags


## -description



The <b>SetCredentialFlags</b> method is used to set the user preference for automatic password caching. When your application prompts the user for a password, you can include a checkbox on the dialog box that the user can select to always have passwords saved. You can then set a flag to maintain that preference.




## -parameters




### -param dwFlags [in]

<b>DWORD</b> containing the credential flags. At this time, the only supported flag is 0x1, which signifies that the user has stated a preference that passwords should be saved automatically.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0fbdad85-d94a-4598-bb25-f733df33692a">IWMSInternalAdminNetSource Interface</a>



<a href="https://msdn.microsoft.com/781b2868-c8e2-4d92-98f2-c2950fac3d9b">IWMSInternalAdminNetSource::GetCredentialFlags</a>



<a href="https://msdn.microsoft.com/c0655ed3-8d14-447a-b74f-054498eb75e9">IWMSInternalAdminNetSource::SetCredentials</a>
 

 

