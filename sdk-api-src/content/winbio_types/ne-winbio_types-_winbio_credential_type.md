---
UID: NE:winbio_types._WINBIO_CREDENTIAL_TYPE
title: "_WINBIO_CREDENTIAL_TYPE"
author: windows-driver-content
description: Defines flags that can be used to filter on the credential type.
old-location: secbiomet\winbio_credential_type.htm
old-project: SecBioMet
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WINBIO_CREDENTIAL_ALL, WINBIO_CREDENTIAL_PASSWORD, WINBIO_CREDENTIAL_TYPE, WINBIO_CREDENTIAL_TYPE enumeration [Windows Biometric Framework API], _WINBIO_CREDENTIAL_TYPE, secbiomet.winbio_credential_type, winbio_types/WINBIO_CREDENTIAL_ALL, winbio_types/WINBIO_CREDENTIAL_PASSWORD, winbio_types/WINBIO_CREDENTIAL_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winbio_types.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_CREDENTIAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_CREDENTIAL_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_CREDENTIAL_TYPE enumeration


## -description


Defines flags that can be used to filter on the credential type. This enumeration is used by the <a href="https://msdn.microsoft.com/c35dd874-c545-418a-b08c-82f9e13e93fb">WinBioSetCredential</a>, <a href="https://msdn.microsoft.com/56a5d510-f2cb-457b-884a-ad08ea21ce01">WinBioRemoveCredential</a>, and <a href="https://msdn.microsoft.com/738b7efb-c796-4f64-95e3-feaaa50ac673">WinBioGetCredentialState</a> functions.


## -enum-fields




### -field WINBIO_CREDENTIAL_PASSWORD

Filters password  credentials.


### -field WINBIO_CREDENTIAL_ALL

Filters all credentials.


## -see-also




<a href="https://msdn.microsoft.com/fd33bc63-cc99-40de-a43b-b0bc7d4c9454">Client Application Enumerations</a>



<a href="https://msdn.microsoft.com/738b7efb-c796-4f64-95e3-feaaa50ac673">WinBioGetCredentialState</a>



<a href="https://msdn.microsoft.com/56a5d510-f2cb-457b-884a-ad08ea21ce01">WinBioRemoveCredential</a>



<a href="https://msdn.microsoft.com/c35dd874-c545-418a-b08c-82f9e13e93fb">WinBioSetCredential</a>
 

 

