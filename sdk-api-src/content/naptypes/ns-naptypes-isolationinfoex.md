---
UID: NS:naptypes.tagIsolationInfoEx
title: IsolationInfoEx (naptypes.h)
description: Defines the extended isolation status of the machine or the connection.
helpviewer_keywords: ["IsolationInfoEx","IsolationInfoEx structure [NAP]","nap.isolationinfoex","naptypes/IsolationInfoEx"]
old-location: nap\isolationinfoex.htm
tech.root: NAP
ms.assetid: 7b361429-015f-4ecc-8569-3075b5b7b85d
ms.date: 12/05/2018
ms.keywords: IsolationInfoEx, IsolationInfoEx structure [NAP], nap.isolationinfoex, naptypes/IsolationInfoEx
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
req.typenames: IsolationInfoEx
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIsolationInfoEx
 - naptypes/tagIsolationInfoEx
 - IsolationInfoEx
 - naptypes/IsolationInfoEx
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
 - IsolationInfoEx
---

# IsolationInfoEx structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>IsolationInfoEx</b> structure defines the extended isolation status of the machine or the connection.

## -struct-fields

### -field isolationState

An <a href="/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a> value that contains the isolation state of a machine.

### -field extendedIsolationState

An <a href="/windows/desktop/api/naptypes/ne-naptypes-extendedisolationstate">ExtendedIsolationState</a> value that contains the extended isolation state of a machine.

### -field probEndTime

A <a href="/windows/desktop/NAP/nap-datatypes">ProbationTime</a> value that contains the time at which a machine should come out from probation.

### -field failureUrl

A <a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a> value that contains a URL to navigate to in the event of failure.

## -see-also

<a href="/windows/desktop/api/naptypes/ns-naptypes-countedstring">CountedString</a>



<a href="/windows/desktop/api/naptypes/ne-naptypes-extendedisolationstate">ExtendedIsolationState</a>



<a href="/windows/desktop/api/naptypes/ne-naptypes-isolationstate">IsolationState</a>



<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>