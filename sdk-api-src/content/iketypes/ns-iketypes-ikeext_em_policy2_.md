---
UID: NS:iketypes.IKEEXT_EM_POLICY2_
title: IKEEXT_EM_POLICY2_
author: windows-sdk-content
description: Is used to store AuthIP's extended mode negotiation policy.
old-location: fwp\ikeext_em_policy2.htm
tech.root: FWP
ms.assetid: 01e3122b-812f-4c01-a514-dc0d513de822
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IKEEXT_EM_POLICY2, IKEEXT_EM_POLICY2 structure [Filtering], IKEEXT_EM_POLICY2_, fwp.ikeext_em_policy2, iketypes/IKEEXT_EM_POLICY2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - iketypes.h
api_name:
 - IKEEXT_EM_POLICY2
product: Windows
targetos: Windows
req.typenames: IKEEXT_EM_POLICY2
req.redist: 
---

# IKEEXT_EM_POLICY2_ structure


## -description


The <b>IKEEXT_EM_POLICY2</b> structure is used to store AuthIP's extended mode negotiation policy.
<div class="alert"><b>Note</b>  <b>IKEEXT_EM_POLICY2</b> is the specific implementation of IKEEXT_EM_POLICY used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/dae56d71-31e0-4746-8bfb-4ade3705278f">IKEEXT_EM_POLICY1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/954a2bb8-eb54-4f41-8a0c-3f2af1190f57">IKEEXT_EM_POLICY0</a>  is available.</div><div> </div>

## -struct-fields




### -field numAuthenticationMethods

Type: <b>UINT32</b>

 Number of authentication methods in the array.


### -field authenticationMethods

Type: <b><a href="https://msdn.microsoft.com/f0bd649e-746d-4802-87fe-d8baec2b252f">IKEEXT_AUTHENTICATION_METHOD2</a>*</b>

size_is(numAuthenticationMethods)

Array of acceptable authentication methods.


### -field initiatorImpersonationType

Type: <b><a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a></b>

Type of impersonation.


## -see-also




<a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



<a href="https://msdn.microsoft.com/f0bd649e-746d-4802-87fe-d8baec2b252f">IKEEXT_AUTHENTICATION_METHOD2</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

