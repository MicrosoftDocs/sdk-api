---
UID: NF:mi.MI_Application_NewSerializer
title: MI_Application_NewSerializer function (mi.h)
description: Retrieves a serializer object that can then be used to serialize instances and classes into various different formats.
helpviewer_keywords: ["MI_Application_NewSerializer","MI_Application_NewSerializer function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewSerializer","wmi_v2.mi_application_newserializer"]
old-location: wmi_v2\mi_application_newserializer.htm
tech.root: wmi_v2
ms.assetid: 9de29d43-0677-4dc9-927f-af7c01179991
ms.date: 12/05/2018
ms.keywords: MI_Application_NewSerializer, MI_Application_NewSerializer function [Windows Management Infrastructure (MI)], mi/MI_Application_NewSerializer, wmi_v2.mi_application_newserializer
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Application_NewSerializer
 - mi/MI_Application_NewSerializer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Application_NewSerializer
---

# MI_Application_NewSerializer function


## -description

Retrieves a serializer object that can then be used to serialize instances and classes into various different formats.

## -parameters

### -param application [in, out]

A pointer to a handle returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a> function.

### -param flags

This parameter must be 0.

### -param format [in]

A string that contains which serializer to use.  This parameter must be L"MI_XML".

### -param serializer [out]

The returned  serializer object.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

Serializers are used to persist <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a> and <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> objects.  A deserializer is then used to re-create the object from its stored form.