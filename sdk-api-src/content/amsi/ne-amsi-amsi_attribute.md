---
UID: NE:amsi.AMSI_ATTRIBUTE
title: AMSI_ATTRIBUTE (amsi.h)
description: Specifies the types of attributes that can be requested by IAmsiStream::GetAttribute.
helpviewer_keywords: ["AMSI_ATTRIBUTE","AMSI_ATTRIBUTE enumeration [Antimalware Scan Interface]","AMSI_ATTRIBUTE_APP_NAME","AMSI_ATTRIBUTE_CONTENT_ADDRESS","AMSI_ATTRIBUTE_CONTENT_NAME","AMSI_ATTRIBUTE_CONTENT_SIZE","AMSI_ATTRIBUTE_SESSION","amsi.amsi_attribute","amsi/AMSI_ATTRIBUTE","amsi/AMSI_ATTRIBUTE_APP_NAME","amsi/AMSI_ATTRIBUTE_CONTENT_ADDRESS","amsi/AMSI_ATTRIBUTE_CONTENT_NAME","amsi/AMSI_ATTRIBUTE_CONTENT_SIZE","amsi/AMSI_ATTRIBUTE_SESSION"]
old-location: amsi\amsi_attribute.htm
tech.root: AMSI
ms.assetid: 19DD293C-71FF-4E40-A2B7-12B4A2D00DBD
ms.date: 12/05/2018
ms.keywords: AMSI_ATTRIBUTE, AMSI_ATTRIBUTE enumeration [Antimalware Scan Interface], AMSI_ATTRIBUTE_APP_NAME, AMSI_ATTRIBUTE_CONTENT_ADDRESS, AMSI_ATTRIBUTE_CONTENT_NAME, AMSI_ATTRIBUTE_CONTENT_SIZE, AMSI_ATTRIBUTE_SESSION, amsi.amsi_attribute, amsi/AMSI_ATTRIBUTE, amsi/AMSI_ATTRIBUTE_APP_NAME, amsi/AMSI_ATTRIBUTE_CONTENT_ADDRESS, amsi/AMSI_ATTRIBUTE_CONTENT_NAME, amsi/AMSI_ATTRIBUTE_CONTENT_SIZE, amsi/AMSI_ATTRIBUTE_SESSION
req.header: amsi.h
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
req.typenames: AMSI_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AMSI_ATTRIBUTE
 - amsi/AMSI_ATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amsi.h
api_name:
 - AMSI_ATTRIBUTE
---

# AMSI_ATTRIBUTE enumeration


## -description

The <b>AMSI_ATTRIBUTE</b> enumeration specifies the types of attributes that can be requested by <a href="/windows/desktop/api/amsi/nf-amsi-iamsistream-getattribute">IAmsiStream::GetAttribute</a>.

## -enum-fields

### -field AMSI_ATTRIBUTE_APP_NAME

Return the name, version, or GUID string of the calling application, copied from a <b>LPWSTR</b>.

### -field AMSI_ATTRIBUTE_CONTENT_NAME

Return the filename, URL, unique script ID, or similar of the content, copied from a <b>LPWSTR</b>.

### -field AMSI_ATTRIBUTE_CONTENT_SIZE

Return the  size of the input, as a <b>ULONGLONG</b>.

### -field AMSI_ATTRIBUTE_CONTENT_ADDRESS

Return the  memory address if the content is fully loaded into memory.

### -field AMSI_ATTRIBUTE_SESSION

Session is used to associate different scan calls, such as if the contents to be scanned belong to the sample original script. Return a <b>PVOID</b> to the next portion of the content to be scanned. Return <b>nullptr</b> if the content is self-contained.

### -field AMSI_ATTRIBUTE_REDIRECT_CHAIN_SIZE

### -field AMSI_ATTRIBUTE_REDIRECT_CHAIN_ADDRESS

### -field AMSI_ATTRIBUTE_ALL_SIZE

### -field AMSI_ATTRIBUTE_ALL_ADDRESS

### -field AMSI_ATTRIBUTE_QUIET