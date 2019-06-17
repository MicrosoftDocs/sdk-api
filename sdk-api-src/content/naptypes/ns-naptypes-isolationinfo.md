---
UID: NS:naptypes.tagIsolationInfo
title: IsolationInfo (naptypes.h)
author: windows-sdk-content
description: Defines the isolation status of the machine or the connection.
old-location: nap\isolationinfo_struct.htm
tech.root: NAP
ms.assetid: ab5e54ab-de5d-489d-bff7-3be4f3973e7a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsolationInfo, IsolationInfo structure [NAP], nap.isolationinfo_struct, naptypes/IsolationInfo
ms.topic: struct
f1_keywords: ["naptypes/IsolationInfo"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - IsolationInfo
product: Windows
targetos: Windows
req.typenames: IsolationInfo
req.redist: 
ms.custom: 19H1
---

# IsolationInfo structure


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>IsolationInfo</b> structure defines the isolation status of the machine or the connection.


## -struct-fields




### -field isolationState

An <a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ne-naptypes-tagisolationstate">IsolationState</a> values that contains the isolation state of a machine.


### -field probEndTime

A <a href="https://docs.microsoft.com/windows/desktop/NAP/nap-datatypes">ProbationTime</a> value that contains the time at which a machine should come out from probation.


### -field failureUrl

A <a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ns-naptypes-tagcountedstring">CountedString</a> value that contains a URL to navigate to in the event of failure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ns-naptypes-tagcountedstring">CountedString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/naptypes/ne-naptypes-tagisolationstate">IsolationState</a>



<a href="https://docs.microsoft.com/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="https://docs.microsoft.com/windows/desktop/NAP/nap-structures">NAP Structures</a>
 

 

