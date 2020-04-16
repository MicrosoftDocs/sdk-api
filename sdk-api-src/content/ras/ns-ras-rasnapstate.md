---
UID: NS:ras._tagRasNapState
title: RASNAPSTATE (ras.h)
description: The Network Access Protection (NAP) variables for a remote access connection.helpviewer_keywords: ["*LPRASNAPSTATE","LPRASNAPSTATE","LPRASNAPSTATE structure pointer [RAS]","RASNAPSTATE","RASNAPSTATE structure [RAS]","ras/LPRASNAPSTATE","ras/RASNAPSTATE","rras.rasnapstate"]
old-location: rras\rasnapstate.htm
tech.root: RRAS
ms.assetid: 1cba931c-041a-4ec6-8c30-db3a02b59ec3
ms.date: 12/05/2018
ms.keywords: '*LPRASNAPSTATE, LPRASNAPSTATE, LPRASNAPSTATE structure pointer [RAS], RASNAPSTATE, RASNAPSTATE structure [RAS], ras/LPRASNAPSTATE, ras/RASNAPSTATE, rras.rasnapstate'
f1_keywords:
- ras/RASNAPSTATE
dev_langs:
- c++
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
targetos: Windows
req.typenames: RASNAPSTATE, *LPRASNAPSTATE
req.redist: 
ms.custom: 19H1
---

# RASNAPSTATE structure


## -description


The RASNAPSTATE structure contains information about the <a href="https://docs.microsoft.com/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection</a> (NAP) variables for a remote access connection.


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes.


### -field dwFlags

Contains information about what members of this structure are set on the return from a call to the <a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetnapstatus">RasGetNapStatus</a> function.


### -field isolationState

An <a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a> value that specifies the isolation NAP state for the RAS connection.


### -field probationTime

Specifies the time required for the connection to come out of quarantine after which the connection will be dropped. A ProbationTime structure is identical to a <b>FILETIME</b> structure.


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a> enumerated type and the ProbationTime structure are declared in naptypes.h.



