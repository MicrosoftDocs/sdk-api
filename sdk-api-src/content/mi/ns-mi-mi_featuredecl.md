---
UID: NS:mi._MI_FeatureDecl
title: MI_FeatureDecl (mi.h)
description: Contains properties that are common to the MI_PropertyDeclMI_ParameterDecland MI_MethodDecl structures.
helpviewer_keywords: ["MI_FeatureDecl","MI_FeatureDecl structure [Windows Management Infrastructure (MI)]","mi/MI_FeatureDecl","wmi_v2.mi_featuredecl"]
old-location: wmi_v2\mi_featuredecl.htm
tech.root: wmi_v2
ms.assetid: 7C669B89-C6D7-45E5-AAD8-A884F4E87659
ms.date: 12/05/2018
ms.keywords: MI_FeatureDecl, MI_FeatureDecl structure [Windows Management Infrastructure (MI)], mi/MI_FeatureDecl, wmi_v2.mi_featuredecl
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
req.typenames: MI_FeatureDecl
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_FeatureDecl
 - mi/_MI_FeatureDecl
 - MI_FeatureDecl
 - mi/MI_FeatureDecl
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
 - MI_FeatureDecl
---

# MI_FeatureDecl structure


## -description

Contains properties that are common to the <a href="/windows/desktop/api/mi/ns-mi-mi_propertydecl">MI_PropertyDecl</a>
<a href="/windows/desktop/api/mi/ns-mi-mi_parameterdecl">MI_ParameterDecl</a> and <a href="/windows/desktop/api/mi/ns-mi-mi_methoddecl">MI_MethodDecl</a> structures.

## -struct-fields

### -field flags

Flags.

### -field code

Hash code: <code>(name[0] &lt;&lt; 16) | (name[len-1] &lt;&lt; 8) | len */</code>

### -field name

Name of this feature.

### -field qualifiers

Describes metadata for classes, properties, methods, and parameters.

### -field numQualifiers

Length of <b>qualifiers</b> array.