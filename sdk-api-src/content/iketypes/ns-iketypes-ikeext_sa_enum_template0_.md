---
UID: NS:iketypes.IKEEXT_SA_ENUM_TEMPLATE0_
title: IKEEXT_SA_ENUM_TEMPLATE0_
author: windows-sdk-content
description: Is an enumeration template used for enumerating IKE/AuthIP security associations (SAs).
old-location: fwp\ikeext_sa_enum_template0.htm
tech.root: FWP
ms.assetid: 69bb80de-e512-4fbd-a62f-40bb211e6b26
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IKEEXT_SA_ENUM_TEMPLATE0, IKEEXT_SA_ENUM_TEMPLATE0 structure [Filtering], IKEEXT_SA_ENUM_TEMPLATE0_, fwp.ikeext_sa_enum_template0, iketypes/IKEEXT_SA_ENUM_TEMPLATE0
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
 - IKEEXT_SA_ENUM_TEMPLATE0
product: Windows
targetos: Windows
req.typenames: IKEEXT_SA_ENUM_TEMPLATE0
req.redist: 
---

# IKEEXT_SA_ENUM_TEMPLATE0_ structure


## -description


The <b>IKEEXT_SA_ENUM_TEMPLATE0</b> structureis an enumeration template used for enumerating IKE/AuthIP security associations (SAs).


## -struct-fields




### -field localSubNet

Matches SAs whose local address is on the specified subnet. Must be of one of the following types.

<ul>
<li>FWP_UINT32</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
<li>FWP_V4_ADDR_MASK</li>
<li>FWP_V6_ADDR_MASK</li>
</ul>
See <a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a> for more information.


### -field remoteSubNet

Matches SAs whose remote address is on the specified subnet. Must be of one of the following types.

<ul>
<li>FWP_UINT32</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
<li>FWP_V4_ADDR_MASK</li>
<li>FWP_V6_ADDR_MASK</li>
</ul>
See <a href="https://msdn.microsoft.com/edc34005-dbc1-45a4-b6c7-fbb8b13fa388">FWP_CONDITION_VALUE0</a> for more information.


### -field localMainModeCertHash

Matches SAs with a matching local main mode SHA thumbprint.  If none exist, this member will have a length of zero.

See <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> for more information.


## -remarks



<b>IKEEXT_SA_ENUM_TEMPLATE0</b> is a specific implementation of IKEEXT_SA_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

