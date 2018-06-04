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

# ISharingConfigurationManager::ShareExists


## -description


Queries whether the <b>Users</b> or <b>Public</b> folder is shared.


## -parameters




### -param dsid [in]

Type: <b><a href="https://msdn.microsoft.com/02d3b664-eeef-4214-99e8-246241103c4e">DEF_SHARE_ID</a></b>

One of the <a href="https://msdn.microsoft.com/02d3b664-eeef-4214-99e8-246241103c4e">DEF_SHARE_ID</a> values that indicates the folder whose sharing state is being checked.


## -returns



Type: <b>HRESULT</b>

S_OK if the folder is shared; otherwise, S_FALSE.




## -remarks



Because as of Windows 7 <b>Public</b> is shared in-place through <b>Users</b>, callers should always check for the Users share first. If a share is found to exist on <b>Users</b>, then it follows that a share exists on <b>Public</b> as well.



