---
UID: NS:iketypes.IKEEXT_CREDENTIALS0_
title: IKEEXT_CREDENTIALS0 (iketypes.h)
author: windows-sdk-content
description: Is used to store multiple credential pairs.
old-location: fwp\ikeext_credentials0.htm
tech.root: fwp
ms.assetid: 048d0a56-5d9b-4a85-b42f-8505eb6a97a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIALS0, IKEEXT_CREDENTIALS0 structure [Filtering], fwp.ikeext_credentials0, iketypes/IKEEXT_CREDENTIALS0
ms.topic: struct
f1_keywords: 
 - "iketypes/IKEEXT_CREDENTIALS0"
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
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
 - Iketypes.h
api_name:
 - IKEEXT_CREDENTIALS0
targetos: Windows
req.typenames: IKEEXT_CREDENTIALS0
req.redist: 
ms.custom: 19H1
---

# IKEEXT_CREDENTIALS0 structure


## -description


The <b>IKEEXT_CREDENTIALS0</b> structure is used to store multiple credential pairs.  
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIALS0</b> is the specific implementation of IKEEXT_CREDENTIALS used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials1_">IKEEXT_CREDENTIALS1</a> is available. For Windows 8, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials2_">IKEEXT_CREDENTIALS2</a> is available.</div><div> </div>

## -struct-fields




### -field numCredentials

Number of <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0_">IKEEXT_CREDENTIAL_PAIR0</a> structures in the array.


### -field credentials

[size_is(numCredentials)]

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0_">IKEEXT_CREDENTIAL_PAIR0</a> structures.


## -remarks



IKE has only 1 pair.

AuthIP
has 1 pair, or 2 pairs if EM was enabled.

MM authentication is always index 0.

EM authentication, if it occurs,
is index 1.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0_">IKEEXT_CREDENTIAL_PAIR0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

