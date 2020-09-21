---
UID: NS:naptypes.tagSoHAttribute
title: SoHAttribute (naptypes.h)
description: Defines the SoH protocol between the SHA/SHV and the NAP system.
helpviewer_keywords: ["SoHAttribute","SoHAttribute structure [NAP]","nap.sohattribute_struct","naptypes/SoHAttribute"]
old-location: nap\sohattribute_struct.htm
tech.root: NAP
ms.assetid: cd954277-27e0-47f4-b4c3-f5335925b8fd
ms.date: 12/05/2018
ms.keywords: SoHAttribute, SoHAttribute structure [NAP], nap.sohattribute_struct, naptypes/SoHAttribute
req.header: naptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: NapTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SoHAttribute
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSoHAttribute
 - naptypes/tagSoHAttribute
 - SoHAttribute
 - naptypes/SoHAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NapTypes.h
api_name:
 - SoHAttribute
---

# SoHAttribute structure


## -description

<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>SoHAttribute</b> structure defines the SoH protocol between the SHA/SHV and the NAP system.

## -struct-fields

### -field type

A <a href="/windows/desktop/NAP/sohattributetype-enum">SoHAttributeType</a> value that defines the attribute type contained in <b>value</b>.

### -field size

The size, in bytes, of the SoH attribute pointed to by <b>value</b> and has a range of 0 to <a href="/windows/desktop/NAP/nap-type-constants">maxSoHAttributeSize</a>.

### -field value

A pointer to a <a href="/windows/desktop/NAP/sohattributevalue-union">SoHAttributeValue</a> structure that contains the SoH attribute value as defined by <b>type</b>.

## -see-also

<a href="/windows/desktop/NAP/nap-reference">NAP Reference</a>



<a href="/windows/desktop/NAP/nap-structures">NAP Structures</a>