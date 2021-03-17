---
UID: NS:naptypes.tagIsolationInfo
title: IsolationInfo (naptypes.h)
description: Defines the isolation status of the machine or the connection.
helpviewer_keywords: ["IsolationInfo","IsolationInfo structure [NAP]","nap.isolationinfo_struct","naptypes/IsolationInfo"]
old-location: nap\isolationinfo_struct.htm
tech.root: NAP
ms.assetid: ab5e54ab-de5d-489d-bff7-3be4f3973e7a
ms.date: 12/05/2018
ms.keywords: IsolationInfo, IsolationInfo structure [NAP], nap.isolationinfo_struct, naptypes/IsolationInfo
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IsolationInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIsolationInfo
 - naptypes/tagIsolationInfo
 - IsolationInfo
 - naptypes/IsolationInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - IsolationInfo
---

# IsolationInfo structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>IsolationInfo</b> structure defines the isolation status of the machine or the connection.

## -struct-fields

### -field isolationState

An <a href="/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a> values that contains the isolation state of a machine.

### -field probEndTime

A <a href="/windows/desktop/NAP/nap-datatypes">ProbationTime</a> value that contains the time at which a machine should come out from probation.

### -field failureUrl

A <a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a> value that contains a URL to navigate to in the event of failure.

## -see-also

<a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a>



<a href="/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a>



<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>