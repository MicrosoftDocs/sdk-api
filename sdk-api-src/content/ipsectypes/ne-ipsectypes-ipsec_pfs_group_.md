---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPSEC_PFS_GROUP_ enumeration


## -description



		The <b>IPSEC_PFS_GROUP</b> enumerated type specifies the Diffie Hellman algorithm that should be used for 
Quick Mode PFS (Perfect Forward Secrecy).


## -enum-fields




### -field IPSEC_PFS_NONE

Specifies no Quick Mode PFS.


### -field IPSEC_PFS_1

Specifies Diffie Hellman group 1.


### -field IPSEC_PFS_2

Specifies Diffie Hellman group 2.


### -field IPSEC_PFS_2048

Specifies Diffie Hellman group 14.


### -field IPSEC_PFS_14

Specifies Diffie Hellman group 14.

<div class="alert"><b>Note</b>  This group was called Diffie Hellman group 2048 when it was introduced.  The name has since been changed to match standard terminology.</div>
<div> </div>
<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012. </div>
<div> </div>

### -field IPSEC_PFS_ECP_256

Specifies Diffie Hellman ECP group 256.


### -field IPSEC_PFS_ECP_384

Specifies Diffie Hellman ECP group 384.


### -field IPSEC_PFS_MM

Use the same Diffie Hellman as the main mode that contains this quick mode.


### -field IPSEC_PFS_24

Specifies Diffie Hellman group 24.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field IPSEC_PFS_MAX

Maximum value for testing only.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">WFP Enumerated Types</a>
 

 

