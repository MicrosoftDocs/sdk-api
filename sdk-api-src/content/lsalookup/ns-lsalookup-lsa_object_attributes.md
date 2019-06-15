---
UID: NS:lsalookup._LSA_OBJECT_ATTRIBUTES
title: LSA_OBJECT_ATTRIBUTES (lsalookup.h)
author: windows-sdk-content
description: The LSA_OBJECT_ATTRIBUTES structure is used with the LsaOpenPolicy function to specify the attributes of the connection to the Policy object.
old-location: security\lsa_object_attributes.htm
tech.root: SecMgmt
ms.assetid: ad05cb52-8e58-46a9-b3e8-0c9c2a24a997
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PLSA_OBJECT_ATTRIBUTES, LSA_OBJECT_ATTRIBUTES, LSA_OBJECT_ATTRIBUTES structure [Security], PLSA_OBJECT_ATTRIBUTES, PLSA_OBJECT_ATTRIBUTES structure pointer [Security], _lsa_lsa_object_attributes, lsalookup/LSA_OBJECT_ATTRIBUTES, lsalookup/PLSA_OBJECT_ATTRIBUTES, security.lsa_object_attributes"
ms.topic: struct
req.header: lsalookup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - LsaLookup.h
api_name:
 - LSA_OBJECT_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: LSA_OBJECT_ATTRIBUTES, *PLSA_OBJECT_ATTRIBUTES
req.redist: 
ms.custom: 19H1
---

# LSA_OBJECT_ATTRIBUTES structure


## -description


The <b>LSA_OBJECT_ATTRIBUTES</b> structure is used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a> function to specify the attributes of the connection to the <a href="https://docs.microsoft.com/windows/desktop/SecMgmt/policy-object">Policy</a> object.

When you call <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a>, initialize the members of this structure to <b>NULL</b> or zero because the function does not use the information.


## -struct-fields




### -field Length

Specifies the size, in bytes, of the <b>LSA_OBJECT_ATTRIBUTES</b> structure.


### -field RootDirectory

Should be <b>NULL</b>.


### -field ObjectName

Should be <b>NULL</b>.


### -field Attributes

Should be zero.


### -field SecurityDescriptor

Should be <b>NULL</b>.


### -field SecurityQualityOfService

Should be <b>NULL</b>.


## -remarks



The <b>LSA_OBJECT_ATTRIBUTES</b> structure is defined in the LsaLookup.h header file.

<b>Windows Server 2008 with SP2 and earlier, Windows Vista with SP2 and earlier, Windows Server 2003, Windows XP/2000:  </b>The <b>LSA_OBJECT_ATTRIBUTES</b> structure is defined in the NTSecAPI.h header file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_quality_of_service">SECURITY_QUALITY_OF_SERVICE</a>
 

 

