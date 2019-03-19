---
UID: NS:iscsidsc.__unnamed_struct_2
title: IKE_AUTHENTICATION_INFORMATION (iscsidsc.h)
author: windows-sdk-content
description: IKE_AUTHENTICATION_INFORMATION structure contains Internet Key Exchange (IKE) authentication information used to establish a secure channel between two key management daemons.
old-location: iscsidisc\ike_authentication_information.htm
tech.root: iSCSIDisc
ms.assetid: d61036f5-a5e8-4c1a-8f99-57fe8e5c5bd0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIKE_AUTHENTICATION_INFORMATION, IKE_AUTHENTICATION_INFORMATION, IKE_AUTHENTICATION_INFORMATION structure [iSCSI Discovery Library API], PIKE_AUTHENTICATION_INFORMATION, PIKE_AUTHENTICATION_INFORMATION structure pointer [iSCSI Discovery Library API], iscsidisc.ike_authentication_information, iscsidsc/IKE_AUTHENTICATION_INFORMATION, iscsidsc/PIKE_AUTHENTICATION_INFORMATION"
ms.topic: struct
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Iscsidsc.h
api_name:
 - IKE_AUTHENTICATION_INFORMATION
product: Windows
targetos: Windows
req.typenames: IKE_AUTHENTICATION_INFORMATION, *PIKE_AUTHENTICATION_INFORMATION
req.redist: 
---

# IKE_AUTHENTICATION_INFORMATION structure


## -description


The <b>IKE_AUTHENTICATION_INFORMATION</b> structure contains Internet Key Exchange (IKE) authentication information used to establish a secure channel between two key management daemons.


## -struct-fields




### -field AuthMethod

A <a href="https://msdn.microsoft.com/be92f3db-93c5-41e3-bd5a-f929f911da39">IKE_AUTHENTICATION_METHOD</a> structure that indicates the authentication method. 


### -field PsKey

A <a href="https://msdn.microsoft.com/52a188b5-6b59-4ea8-89e0-d05440344dde">IKE_AUTHENTICATION_PRESHARED_KEY</a> structure that contains the preshared key that establishes a secure channel between two key management daemons.


## -see-also




<a href="https://msdn.microsoft.com/be92f3db-93c5-41e3-bd5a-f929f911da39">IKE_AUTHENTICATION_METHOD</a>



<a href="https://msdn.microsoft.com/52a188b5-6b59-4ea8-89e0-d05440344dde">IKE_AUTHENTICATION_PRESHARED_KEY</a>
 

 

