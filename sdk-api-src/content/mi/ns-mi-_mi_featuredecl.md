---
UID: NS:mi._MI_FeatureDecl
title: "_MI_FeatureDecl"
author: windows-sdk-content
description: Contains properties that are common to the MI_PropertyDeclMI_ParameterDecl and MI_MethodDecl structures.
old-location: wmi_v2\mi_featuredecl.htm
old-project: wmi_v2
ms.assetid: 7C669B89-C6D7-45E5-AAD8-A884F4E87659
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_FeatureDecl, MI_FeatureDecl structure [Windows Management Infrastructure (MI)], _MI_FeatureDecl, mi/MI_FeatureDecl, wmi_v2.mi_featuredecl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MI_FeatureDecl
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_FeatureDecl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_FeatureDecl structure


## -description


Contains properties that are common to the <a href="https://msdn.microsoft.com/bc5e5c1e-3483-4762-8063-047308dc3652">MI_PropertyDecl</a>
<a href="https://msdn.microsoft.com/09ad6ea4-09ae-428b-9df9-414043044d6a">MI_ParameterDecl</a>
and <a href="https://msdn.microsoft.com/50087394-44C2-4CE5-8952-9795FE9B236A">MI_MethodDecl</a> structures.


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

