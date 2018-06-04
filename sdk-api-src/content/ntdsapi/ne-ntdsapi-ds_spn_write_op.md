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

# DS_SPN_WRITE_OP enumeration


## -description


The <b>DS_SPN_WRITE_OP</b> enumeration identifies the type of write operation that should be performed by the <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a> function.


## -enum-fields




### -field DS_SPN_ADD_SPN_OP

Adds the specified service principal names (SPNs) to the object identified by the <i>pszAccount</i> parameter in <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>.


### -field DS_SPN_REPLACE_SPN_OP

Removes all SPNs currently registered on the account identified by the <i>pszAccount</i> parameter in <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a> and replaces them with the SPNs specified  by the <i>rpszSpn</i> parameter in <b>DsWriteAccountSpn</b>.


### -field DS_SPN_DELETE_SPN_OP

Deletes the specified SPNs from the object identified by the <i>pszAccount</i> parameter in <a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>.


## -see-also




<a href="https://msdn.microsoft.com/2b555f6b-643d-4fa0-9aca-701e6b3313fa">DsWriteAccountSpn</a>



<a href="https://msdn.microsoft.com/eafa3285-4474-4077-a6ad-b37f8211e7e6">Enumerations in Active Directory Domain Services</a>
 

 

