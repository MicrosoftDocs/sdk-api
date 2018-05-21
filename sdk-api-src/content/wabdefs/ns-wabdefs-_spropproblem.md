---
UID: NS:wabdefs._SPropProblem
title: "_SPropProblem"
author: windows-driver-content
description: Do not use. Describes an error relating to an operation involving a property.
old-location: wab\_wab_SPropProblem.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\spropproblem.htm
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*LPSPropProblem, SPropProblem, SPropProblem structure [Windows Address Book], _SPropProblem, _wab_SPropProblem, wab._wab_SPropProblem, wabdefs/SPropProblem"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SPropProblem, *LPSPropProblem
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wabdefs.h
api_name:
-	SPropProblem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# _SPropProblem structure


## -description


Do not use. Describes an error relating to an operation involving a property.


## -struct-fields




### -field ulIndex

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the index value in an array of property tags.


### -field ulPropTag

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the property tag for the property with the error.


### -field scode

Type: <b>SCODE</b>

Variable of type <b>SCODE</b> that specifies the error value that describes the problem with the property.

