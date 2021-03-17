---
UID: NS:ndhelper.tagHelperAttributeInfo
title: HelperAttributeInfo (ndhelper.h)
description: The HelperAttributeInfo structure contains the name of the helper attribute and its type.
helpviewer_keywords: ["*PHelperAttributeInfo","HelperAttributeInfo","HelperAttributeInfo structure [NDF]","HelperAttributeInfo","*PHelperAttributeInfo","HelperAttributeInfo","*PHelperAttributeInfo structure [NDF]","ndf.helperattributeinfo","ndhelper/HelperAttributeInfo"]
old-location: ndf\helperattributeinfo.htm
tech.root: NDF
ms.assetid: a4de3031-7199-4537-a97e-f33059383d6b
ms.date: 12/05/2018
ms.keywords: '*PHelperAttributeInfo, HelperAttributeInfo, HelperAttributeInfo structure [NDF], HelperAttributeInfo,*PHelperAttributeInfo, HelperAttributeInfo,*PHelperAttributeInfo structure [NDF], ndf.helperattributeinfo, ndhelper/HelperAttributeInfo'
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HelperAttributeInfo, *PHelperAttributeInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHelperAttributeInfo
 - ndhelper/tagHelperAttributeInfo
 - PHelperAttributeInfo
 - ndhelper/PHelperAttributeInfo
 - HelperAttributeInfo
 - ndhelper/HelperAttributeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndhelper.h
api_name:
 - HelperAttributeInfo, *PHelperAttributeInfo
---

# HelperAttributeInfo structure


## -description

The <b>HelperAttributeInfo</b> structure contains the name of the helper attribute and its type.

## -struct-fields

### -field pwszName

Type: <b>[string] LPWSTR</b>

Pointer to a null-terminated string that contains the name of the helper attribute.

### -field type

Type: <b><a href="/windows/desktop/api/ndattrib/ne-ndattrib-attribute_type">ATTRIBUTE_TYPE</a></b>

The type of helper attribute.

## -see-also

<a href="/windows/desktop/api/ndattrib/ne-ndattrib-attribute_type">ATTRIBUTE_TYPE</a>



<a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a>