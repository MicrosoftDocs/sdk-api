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

# _tagRasNapState structure


## -description


The RASNAPSTATE structure contains information about the <a href="https://msdn.microsoft.com/f562f5f1-c05a-4e4e-bcd9-a302c61f2a5e">Network Access Protection</a> (NAP) variables for a remote access connection.


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes.


### -field dwFlags

Contains information about what members of this structure are set on the return from a call to the <a href="https://msdn.microsoft.com/7f36f93f-7e07-4ad8-923f-59146bda4687">RasGetNapStatus</a> function.


### -field isolationState

An <a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">IsolationState</a> value that specifies the isolation NAP state for the RAS connection.


### -field probationTime

Specifies the time required for the connection to come out of quarantine after which the connection will be dropped. A ProbationTime structure is identical to a <b>FILETIME</b> structure.


## -remarks



The <a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">IsolationState</a> enumerated type and the ProbationTime structure are declared in naptypes.h.



