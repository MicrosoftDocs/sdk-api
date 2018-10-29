---
UID: NS:ras._tagRasNapState
title: "_tagRasNapState"
author: windows-sdk-content
description: The Network Access Protection (NAP) variables for a remote access connection.
old-location: rras\rasnapstate.htm
tech.root: RRAS
ms.assetid: 1cba931c-041a-4ec6-8c30-db3a02b59ec3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*LPRASNAPSTATE, LPRASNAPSTATE, LPRASNAPSTATE structure pointer [RAS], RASNAPSTATE, RASNAPSTATE structure [RAS], _tagRasNapState, ras/LPRASNAPSTATE, ras/RASNAPSTATE, rras.rasnapstate"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ras.h
api_name:
 - RASNAPSTATE
product: Windows
targetos: Windows
req.typenames: RASNAPSTATE, *LPRASNAPSTATE
req.redist: 
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



