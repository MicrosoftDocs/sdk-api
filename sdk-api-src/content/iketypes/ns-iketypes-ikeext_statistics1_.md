---
UID: NS:iketypes.IKEEXT_STATISTICS1_
title: IKEEXT_STATISTICS1_
author: windows-sdk-content
description: Stores various IKE, AuthIP, and IKEv2 statistics.
old-location: fwp\ikeext_statistics1.htm
tech.root: fwp
ms.assetid: 73c36ea1-d009-4724-8b1c-54503ad57e4d
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IKEEXT_STATISTICS1, IKEEXT_STATISTICS1 structure [Filtering], IKEEXT_STATISTICS1_, fwp.ikeext_statistics1, iketypes/IKEEXT_STATISTICS1
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IKEEXT_STATISTICS1
product: Windows
targetos: Windows
req.typenames: IKEEXT_STATISTICS1
req.redist: 
---

# IKEEXT_STATISTICS1_ structure


## -description


The <a href="https://msdn.microsoft.com/aefacc39-92a5-4d73-ac3c-0b5bf1407a90">IKEEXT_STATISTICS1</a> structure stores various IKE, AuthIP, and IKEv2 statistics.
<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/aefacc39-92a5-4d73-ac3c-0b5bf1407a90">IKEEXT_STATISTICS1</a> is the specific implementation of IKEEXT_STATISTICS used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <b>IKEEXT_STATISTICS0</b> is available.</div><div> </div>

## -struct-fields




### -field ikeStatistics

Statistics specific to IKE.

See <a href="https://msdn.microsoft.com/3b5fdf04-e3a6-4658-a53d-66928b5682f5">IKEEXT_KEYMODULE_STATISTICS1</a> for more information.


### -field authipStatistics

Statistics specific to AuthIP.

See <a href="https://msdn.microsoft.com/3b5fdf04-e3a6-4658-a53d-66928b5682f5">IKEEXT_KEYMODULE_STATISTICS1</a> for more information.


### -field ikeV2Statistics

 


### -field commonStatistics

Statistics common to IKE, AuthIP, and IKEv2.

See <a href="https://msdn.microsoft.com/d2c473d7-921f-4175-8406-8ab24d7f74f4">IKEEXT_COMMON_STATISTICS1</a> for more information.


#### - ikev2Statistics

Statistics specific to IKEv2.

See <a href="https://msdn.microsoft.com/3b5fdf04-e3a6-4658-a53d-66928b5682f5">IKEEXT_KEYMODULE_STATISTICS1</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

