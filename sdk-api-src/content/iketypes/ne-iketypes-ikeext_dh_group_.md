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

# IKEEXT_DH_GROUP_ enumeration


## -description



		The <b>IKEEXT_DH_GROUP</b> enumerated type specifies the type of Diffie Hellman group used for Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) key generation.


## -enum-fields




### -field IKEEXT_DH_GROUP_NONE

Specifies no Diffie Hellman group. Available only for AuthIP.


### -field IKEEXT_DH_GROUP_1

Specifies  Diffie Hellman group 1.


### -field IKEEXT_DH_GROUP_2

Specifies  Diffie Hellman group 2.


### -field IKEEXT_DH_GROUP_14

Specifies  Diffie Hellman group 14.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012. </div>
<div> </div>

### -field IKEEXT_DH_GROUP_2048

Specifies  Diffie Hellman group 14.

<div class="alert"><b>Note</b>  This group was called Diffie Hellman group 2048 when it was introduced.  The name has since been changed to match standard terminology.</div>
<div> </div>

### -field IKEEXT_DH_ECP_256

Specifies Diffie Hellman ECP group 256.


### -field IKEEXT_DH_ECP_384

Specifies Diffie Hellman ECP group 384.


### -field IKEEXT_DH_GROUP_24

Specifies  Diffie Hellman group 24.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field IKEEXT_DH_GROUP_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

