---
UID: NE:winbio_types._WINBIO_CREDENTIAL_STATE
title: "_WINBIO_CREDENTIAL_STATE"
author: windows-driver-content
description: Defines values that specify whether a credential has been associated with the biometric data for an end user.
old-location: secbiomet\winbio_credential_state.htm
old-project: SecBioMet
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PWINBIO_CREDENTIAL_STATE, PWINBIO_CREDENTIAL_STATE, PWINBIO_CREDENTIAL_STATE enumeration pointer [Windows Biometric Framework API], WINBIO_CREDENTIAL_NOT_SET, WINBIO_CREDENTIAL_SET, WINBIO_CREDENTIAL_STATE, WINBIO_CREDENTIAL_STATE enumeration [Windows Biometric Framework API], _WINBIO_CREDENTIAL_STATE, secbiomet.winbio_credential_state, winbio_types/PWINBIO_CREDENTIAL_STATE, winbio_types/WINBIO_CREDENTIAL_NOT_SET, winbio_types/WINBIO_CREDENTIAL_SET, winbio_types/WINBIO_CREDENTIAL_STATE"
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
req.typenames: WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_CREDENTIAL_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_CREDENTIAL_STATE enumeration


## -description


Defines values that specify whether a credential has been associated with the biometric data for an end user. This enumeration is used by the <a href="https://msdn.microsoft.com/738b7efb-c796-4f64-95e3-feaaa50ac673">WinBioGetCredentialState</a> function.


## -enum-fields




### -field WINBIO_CREDENTIAL_NOT_SET

A credential has been associated with the end user.


### -field WINBIO_CREDENTIAL_SET

A credential has not been associated with the end user.


## -see-also




<a href="https://msdn.microsoft.com/fd33bc63-cc99-40de-a43b-b0bc7d4c9454">Client Application Enumerations</a>



<a href="https://msdn.microsoft.com/738b7efb-c796-4f64-95e3-feaaa50ac673">WinBioGetCredentialState</a>
 

 

