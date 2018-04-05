---
UID: NE:winbio_types._WINBIO_CREDENTIAL_FORMAT
title: "_WINBIO_CREDENTIAL_FORMAT"
author: windows-driver-content
description: Defines flags that can be used to specify the end-user credential format.
old-location: secbiomet\winbio_credential_format.htm
old-project: SecBioMet
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WINBIO_CREDENTIAL_FORMAT, WINBIO_CREDENTIAL_FORMAT enumeration [Windows Biometric Framework API], WINBIO_PASSWORD_GENERIC, WINBIO_PASSWORD_PACKED, WINBIO_PASSWORD_PROTECTED, _WINBIO_CREDENTIAL_FORMAT, secbiomet.winbio_credential_format, winbio_types/WINBIO_CREDENTIAL_FORMAT, winbio_types/WINBIO_PASSWORD_GENERIC, winbio_types/WINBIO_PASSWORD_PACKED, winbio_types/WINBIO_PASSWORD_PROTECTED
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winbio_types.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINBIO_CREDENTIAL_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winbio_types.h
api_name:
-	WINBIO_CREDENTIAL_FORMAT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_CREDENTIAL_FORMAT enumeration


## -description


Defines flags that can be used to specify the end-user credential format. This enumeration is used by the <a href="https://msdn.microsoft.com/c35dd874-c545-418a-b08c-82f9e13e93fb">WinBioSetCredential</a> function.


## -enum-fields




### -field WINBIO_PASSWORD_GENERIC

The password is in a generic format.


### -field WINBIO_PASSWORD_PACKED

The password is in a compressed format.


### -field WINBIO_PASSWORD_PROTECTED

The password credential was wrapped with <a href="https://msdn.microsoft.com/1e299dfb-2ffe-463c-9e2c-b7774a2216e3">CredProtect</a>.


## -see-also




<a href="https://msdn.microsoft.com/fd33bc63-cc99-40de-a43b-b0bc7d4c9454">Client Application Enumerations</a>



<a href="https://msdn.microsoft.com/c35dd874-c545-418a-b08c-82f9e13e93fb">WinBioSetCredential</a>
 

 

