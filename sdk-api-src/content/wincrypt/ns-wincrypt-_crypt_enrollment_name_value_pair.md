---
UID: NS:wincrypt._CRYPT_ENROLLMENT_NAME_VALUE_PAIR
title: "_CRYPT_ENROLLMENT_NAME_VALUE_PAIR"
author: windows-sdk-content
description: Used to create certificate requests on behalf of a user.
old-location: security\crypt_enrollment_name_value_pair.htm
old-project: SecCrypto
ms.assetid: 996bd28e-73c1-494e-957c-8dd4c7b8e064
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PCRYPT_ENROLLMENT_NAME_VALUE_PAIR, CRYPT_ENROLLMENT_NAME_VALUE_PAIR, CRYPT_ENROLLMENT_NAME_VALUE_PAIR structure [Security], _CRYPT_ENROLLMENT_NAME_VALUE_PAIR, _crypto2_crypt_enrollment_name_value_pair, security.crypt_enrollment_name_value_pair, wincrypt/CRYPT_ENROLLMENT_NAME_VALUE_PAIR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
tech.root: 
req.typenames: CRYPT_ENROLLMENT_NAME_VALUE_PAIR, *PCRYPT_ENROLLMENT_NAME_VALUE_PAIR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_ENROLLMENT_NAME_VALUE_PAIR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_ENROLLMENT_NAME_VALUE_PAIR structure


## -description


The <b>CRYPT_ENROLLMENT_NAME_VALUE_PAIR</b> structure is used to create certificate requests on behalf of a user.


## -struct-fields




### -field pwszName

Name of a certificate requester.


### -field pwszValue

Name of the user for whom the certificate is being requested.

