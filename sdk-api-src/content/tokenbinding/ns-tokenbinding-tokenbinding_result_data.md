---
UID: NS:tokenbinding.TOKENBINDING_RESULT_DATA
title: TOKENBINDING_RESULT_DATA (tokenbinding.h)
description: Contains data about the result of generating a token binding or verifying one of the token bindings in a token binding message.
helpviewer_keywords: ["TOKENBINDING_RESULT_DATA","TOKENBINDING_RESULT_DATA structure [Security]","security.tokenbinding_result_data","tokenbinding/TOKENBINDING_RESULT_DATA"]
old-location: security\tokenbinding_result_data.htm
tech.root: security
ms.assetid: 6C34E174-CCC4-451D-82C3-C410C8C92C8C
ms.date: 12/05/2018
ms.keywords: TOKENBINDING_RESULT_DATA, TOKENBINDING_RESULT_DATA structure [Security], security.tokenbinding_result_data, tokenbinding/TOKENBINDING_RESULT_DATA
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: TOKENBINDING_RESULT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TOKENBINDING_RESULT_DATA
 - tokenbinding/TOKENBINDING_RESULT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tokenbinding.h
api_name:
 - TOKENBINDING_RESULT_DATA
---

# TOKENBINDING_RESULT_DATA structure


## -description

Contains data about the result of generating a token binding or verifying one of the token bindings in a token binding message.

## -struct-fields

### -field bindingType

### -field identifierSize

The size of the <a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_identifier">TOKENBINDING_IDENTIFIER</a> structure that the <b>identifierData</b> member points to, in bytes.

### -field identifierData

Pointer to the token binding identifier for the token binding that was generated or verified.

### -field extensionFormat

The format to use to interpret the data in the <i>extensionData</i> parameter. This value must be <b>TOKENBINDING_EXTENSION_FORMAT_UNDEFINED</b>.

### -field extensionSize

The size of the buffer that the <b>extensionData</b> member points to, in bytes.

### -field extensionData

A pointer to a buffer that contains extension data. The value of the <i>extensionFormat</i> parameter determines how to interpret this data.

## -see-also

<a href="/windows/desktop/api/tokenbinding/ne-tokenbinding-tokenbinding_extension_format">TOKENBINDING_EXTENSION_FORMAT</a>



<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_identifier">TOKENBINDING_IDENTIFIER</a>



<a href="/windows/desktop/api/tokenbinding/ns-tokenbinding-tokenbinding_result_list">TOKENBINDING_RESULT_LIST</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggeneratebinding">TokenBindingGenerateBinding</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindingverifymessage">TokenBindingVerifyMessage</a>