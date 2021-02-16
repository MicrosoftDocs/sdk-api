---
UID: NS:setupapi._SP_CLASSIMAGELIST_DATA
title: SP_CLASSIMAGELIST_DATA (setupapi.h)
description: An SP_CLASSIMAGELIST_DATA structure describes a class image list.
helpviewer_keywords: ["*PSP_CLASSIMAGELIST_DATA","PSP_CLASSIMAGELIST_DATA","PSP_CLASSIMAGELIST_DATA structure pointer [Device and Driver Installation]","SP_CLASSIMAGELIST_DATA","SP_CLASSIMAGELIST_DATA structure [Device and Driver Installation]","devinst.sp_classimagelist_data","di-struct_2d2e73bd-5f18-49d1-96ad-639bc0ad658e.xml","setupapi/PSP_CLASSIMAGELIST_DATA","setupapi/SP_CLASSIMAGELIST_DATA"]
old-location: devinst\sp_classimagelist_data.htm
tech.root: devinst
ms.assetid: 89ed9dbd-3c5e-43ff-bbd0-fd6cc8c6e6ab
ms.date: 12/05/2018
ms.keywords: '*PSP_CLASSIMAGELIST_DATA, PSP_CLASSIMAGELIST_DATA, PSP_CLASSIMAGELIST_DATA structure pointer [Device and Driver Installation], SP_CLASSIMAGELIST_DATA, SP_CLASSIMAGELIST_DATA structure [Device and Driver Installation], devinst.sp_classimagelist_data, di-struct_2d2e73bd-5f18-49d1-96ad-639bc0ad658e.xml, setupapi/PSP_CLASSIMAGELIST_DATA, setupapi/SP_CLASSIMAGELIST_DATA'
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: SP_CLASSIMAGELIST_DATA, *PSP_CLASSIMAGELIST_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_CLASSIMAGELIST_DATA
 - setupapi/_SP_CLASSIMAGELIST_DATA
 - PSP_CLASSIMAGELIST_DATA
 - setupapi/PSP_CLASSIMAGELIST_DATA
 - SP_CLASSIMAGELIST_DATA
 - setupapi/SP_CLASSIMAGELIST_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_CLASSIMAGELIST_DATA
---

# SP_CLASSIMAGELIST_DATA structure


## -description

An SP_CLASSIMAGELIST_DATA structure describes a class image list.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_CLASSIMAGE_DATA structure.

### -field ImageList

A handle to the class image list.

### -field Reserved

Reserved. For internal use only.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdidestroyclassimagelist">SetupDiDestroyClassImageList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimageindex">SetupDiGetClassImageIndex</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassimagelist">SetupDiGetClassImageList</a>