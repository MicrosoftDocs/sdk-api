---
UID: NE:slpublic._tagSL_ACTIVATION_TYPE
title: SL_ACTIVATION_TYPE (slpublic.h)
description: Represents the type of offline activation for a license.
helpviewer_keywords: ["SL_ACTIVATION_TYPE","SL_ACTIVATION_TYPE enumeration [Security]","SL_ACTIVATION_TYPE_ACTIVE_DIRECTORY","SL_ACTIVATION_TYPE_DEFAULT","security.sl_activation_type","slpublic/SL_ACTIVATION_TYPE","slpublic/SL_ACTIVATION_TYPE_ACTIVE_DIRECTORY","slpublic/SL_ACTIVATION_TYPE_DEFAULT"]
old-location: security\sl_activation_type.htm
tech.root: security
ms.assetid: e16a4e43-f7ef-43a3-a268-5f644340274c
ms.date: 12/05/2018
ms.keywords: SL_ACTIVATION_TYPE, SL_ACTIVATION_TYPE enumeration [Security], SL_ACTIVATION_TYPE_ACTIVE_DIRECTORY, SL_ACTIVATION_TYPE_DEFAULT, security.sl_activation_type, slpublic/SL_ACTIVATION_TYPE, slpublic/SL_ACTIVATION_TYPE_ACTIVE_DIRECTORY, slpublic/SL_ACTIVATION_TYPE_DEFAULT
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: SL_ACTIVATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSL_ACTIVATION_TYPE
 - slpublic/_tagSL_ACTIVATION_TYPE
 - SL_ACTIVATION_TYPE
 - slpublic/SL_ACTIVATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - slpublic.h
api_name:
 - SL_ACTIVATION_TYPE
---

# SL_ACTIVATION_TYPE enumeration


## -description

Represents the type of offline activation for a license. This 	enumeration is used by the <b>type</b> member of the <a href="/windows/desktop/api/slpublic/ns-slpublic-sl_activation_info_header">SL_ACTIVATION_INFO_HEADER</a> structure.

## -enum-fields

### -field SL_ACTIVATION_TYPE_DEFAULT:0

Retail phone activation.

### -field SL_ACTIVATION_TYPE_ACTIVE_DIRECTORY:1

The product activation is through Active Directory.

## -see-also

<a href="/windows/desktop/api/slpublic/ns-slpublic-sl_activation_info_header">SL_ACTIVATION_INFO_HEADER</a>
