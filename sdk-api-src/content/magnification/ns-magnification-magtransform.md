---
UID: NS:magnification.tagMAGTRANSFORM
title: MAGTRANSFORM
author: windows-sdk-content
description: Describes a transformation matrix that a magnifier control uses to magnify screen content.
old-location: magapi\magapi_magtransform.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\structures\magtransformstruct.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMAGTRANSFORM, MAGTRANSFORM, MAGTRANSFORM structure [Magnification API], PMAGTRANSFORM, PMAGTRANSFORM structure pointer [Magnification API], magapi.magapi_magtransform, magapi_magtransform, magnification/MAGTRANSFORM, magnification/PMAGTRANSFORM"
ms.topic: struct
req.header: magnification.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Magnification.h
api_name:
 - MAGTRANSFORM
product: Windows
targetos: Windows
req.typenames: MAGTRANSFORM, *PMAGTRANSFORM
req.redist: 
---

# MAGTRANSFORM structure


## -description


Describes a transformation matrix that a magnifier control uses to magnify screen content.


## -struct-fields




### -field v

Type: <b>float[3]</b>

The transformation matrix.


## -remarks



The transformation matrix is 

 (<i>n</i>, 0.0, 0.0)

 (0.0, <i>n</i>, 0.0)

 (0.0, 0.0, 1.0) 

where <i>n</i> is the magnification factor.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692391(v=VS.85).aspx">MagGetWindowTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692398(v=VS.85).aspx">MagSetWindowTransform</a>



<b>Reference</b>
 

 

