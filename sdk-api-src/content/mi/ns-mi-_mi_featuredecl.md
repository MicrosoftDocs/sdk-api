---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

