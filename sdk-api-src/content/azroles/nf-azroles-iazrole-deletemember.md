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

# IAzRole::DeleteMember


## -description


The <b>DeleteMember</b> method removes  the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form from the list of Windows  accounts that belong to the role.


## -parameters




### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of Windows  accounts that belong to the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of SIDs of Windows accounts that belong to the role in text form, use the <a href="https://msdn.microsoft.com/03391842-fc8a-4dc2-878e-4fe1c41cc4dd">Members</a> property.



