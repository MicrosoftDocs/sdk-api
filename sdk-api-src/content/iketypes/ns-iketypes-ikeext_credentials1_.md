---
UID: NS:iketypes.IKEEXT_CREDENTIALS1_
title: IKEEXT_CREDENTIALS1_
author: windows-sdk-content
description: Is used to store multiple credential pairs.
old-location: fwp\ikeext_credentials1.htm
tech.root: fwp
ms.assetid: dbd895bd-a720-4c8e-a2e7-f5614d69922c
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IKEEXT_CREDENTIALS1, IKEEXT_CREDENTIALS1 structure [Filtering], IKEEXT_CREDENTIALS1_, fwp.ikeext_credentials1, iketypes/IKEEXT_CREDENTIALS1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IKEEXT_CREDENTIALS1
product: Windows
targetos: Windows
req.typenames: IKEEXT_CREDENTIALS1
req.redist: 
---

# IKEEXT_CREDENTIALS1_ structure


## -description


The <b>IKEEXT_CREDENTIALS1</b> structure is used to store multiple credential pairs.
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIALS1</b> is the specific implementation of IKEEXT_CREDENTIALS used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/4099b6e7-0b3b-40ea-821c-3ff28a6f788f">IKEEXT_CREDENTIALS2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/048d0a56-5d9b-4a85-b42f-8505eb6a97a9">IKEEXT_CREDENTIALS0</a> is available.</div><div> </div>

## -struct-fields




### -field numCredentials

Number of <a href="https://msdn.microsoft.com/fe18503d-fd1c-45b6-86c7-9b452036f8c8">IKEEXT_CREDENTIAL_PAIR1</a> structures in the array.


### -field credentials

[size_is(numCredentials)]

Pointer to an array of <a href="https://msdn.microsoft.com/fe18503d-fd1c-45b6-86c7-9b452036f8c8">IKEEXT_CREDENTIAL_PAIR1</a> structures.


## -remarks



IKE and IKEv2 have only 1 pair.

AuthIP
has 1 pair, or 2 pairs if EM was enabled.

MM authentication is always index 0.

EM authentication, if it occurs,
is index 1.




## -see-also




<a href="https://msdn.microsoft.com/fe18503d-fd1c-45b6-86c7-9b452036f8c8">IKEEXT_CREDENTIAL_PAIR1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

