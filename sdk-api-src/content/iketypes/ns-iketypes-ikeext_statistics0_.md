---
UID: NS:iketypes.IKEEXT_STATISTICS0_
title: IKEEXT_STATISTICS0_
author: windows-sdk-content
description: Stores various IKE/AuthIP statistics.
old-location: fwp\ikeext_statistics0.htm
tech.root: fwp
ms.assetid: aefacc39-92a5-4d73-ac3c-0b5bf1407a90
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IKEEXT_STATISTICS0, IKEEXT_STATISTICS0 structure [Filtering], IKEEXT_STATISTICS0_, fwp.ikeext_statistics0, iketypes/IKEEXT_STATISTICS0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - IKEEXT_STATISTICS0
product: Windows
targetos: Windows
req.typenames: IKEEXT_STATISTICS0
req.redist: 
---

# IKEEXT_STATISTICS0_ structure


## -description


The <b>IKEEXT_STATISTICS0</b> structure stores various IKE/AuthIP statistics.
<div class="alert"><b>Note</b>  <b>IKEEXT_STATISTICS0</b> is the specific implementation of IKEEXT_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/73c36ea1-d009-4724-8b1c-54503ad57e4d">IKEEXT_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field ikeStatistics

Statistics specific to IKE.

See <a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a> for more information.


### -field authipStatistics

Statistics specific to AuthIP.

See <a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a> for more information.


### -field commonStatistics

Statistics common to IKE and AuthIP.

See <a href="https://msdn.microsoft.com/a53ef735-3223-4ff5-9b2a-d40ab0f53570">IKEEXT_COMMON_STATISTICS0</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

