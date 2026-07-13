---
UID: NS:wincred._CREDENTIAL_ATTRIBUTEA
title: CREDENTIAL_ATTRIBUTEA (wincred.h)
description: The CREDENTIAL_ATTRIBUTE structure contains an application-defined attribute of the credential. An attribute is a keyword-value pair. It is up to the application to define the meaning of the attribute. (ANSI)
helpviewer_keywords: ["*PCREDENTIAL_ATTRIBUTEA","CREDENTIAL_ATTRIBUTE","CREDENTIAL_ATTRIBUTE structure [Security]","CREDENTIAL_ATTRIBUTEA","PCREDENTIAL_ATTRIBUTE","PCREDENTIAL_ATTRIBUTE structure pointer [Security]","_cred_credential_attribute","security.credential_attribute","wincred/CREDENTIAL_ATTRIBUTE","wincred/PCREDENTIAL_ATTRIBUTE"]
old-location: security\credential_attribute.htm
tech.root: security
ms.assetid: eb46766c-5f05-4e4a-9550-173347f156d9
ms.date: 12/05/2018
ms.keywords: '*PCREDENTIAL_ATTRIBUTEA, CREDENTIAL_ATTRIBUTE, CREDENTIAL_ATTRIBUTE structure [Security], CREDENTIAL_ATTRIBUTEA, PCREDENTIAL_ATTRIBUTE, PCREDENTIAL_ATTRIBUTE structure pointer [Security], _cred_credential_attribute, security.credential_attribute, wincred/CREDENTIAL_ATTRIBUTE, wincred/PCREDENTIAL_ATTRIBUTE'
req.header: wincred.h
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
targetos: Windows
req.typenames: CREDENTIAL_ATTRIBUTEA, *PCREDENTIAL_ATTRIBUTEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_ATTRIBUTEA
 - wincred/_CREDENTIAL_ATTRIBUTEA
 - PCREDENTIAL_ATTRIBUTEA
 - wincred/PCREDENTIAL_ATTRIBUTEA
 - CREDENTIAL_ATTRIBUTEA
 - wincred/CREDENTIAL_ATTRIBUTEA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - CREDENTIAL_ATTRIBUTE
---

# CREDENTIAL_ATTRIBUTEA structure


## -description

The <b>CREDENTIAL_ATTRIBUTE</b> structure contains an application-defined attribute of the credential. An attribute is a keyword-value pair. It is up to the application to define the meaning of the attribute.

## -struct-fields

### -field Keyword

Name of the application-specific attribute. Names should be of the form &lt;CompanyName&gt;_&lt;Name&gt;. 




This member cannot be longer than CRED_MAX_STRING_LENGTH (256) characters.

### -field Flags

Identifies characteristics of the credential attribute. This member is reserved and should be originally initialized as zero and not otherwise altered to permit future enhancement.

### -field ValueSize

Length of <b>Value</b> in bytes. This member cannot be larger than CRED_MAX_VALUE_SIZE (256).

### -field Value

Data associated with the attribute. By convention, if <b>Value</b> is a text string, then  <b>Value</b> should not include the trailing zero character and should be in UNICODE. 




Credentials are expected to be portable. The application should take care to ensure that the data in value is portable. It is the responsibility of the application to define the byte-endian and alignment of the data in <b>Value</b>.

## -remarks

> [!NOTE]
> The wincred.h header defines CREDENTIAL_ATTRIBUTE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

