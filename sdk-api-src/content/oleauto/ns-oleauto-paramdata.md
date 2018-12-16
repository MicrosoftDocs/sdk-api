---
UID: NS:oleauto.tagPARAMDATA
title: PARAMDATA
author: windows-sdk-content
description: Describes a parameter accepted by a method or property.
old-location: automat\paramdata.htm
tech.root: automat
ms.assetid: 3166eac0-7e07-47e1-9bca-60b15cbdf971
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPPARAMDATA, LPPARAMDATA, LPPARAMDATA structure pointer [Automation], PARAMDATA, PARAMDATA structure [Automation], _oa96_PARAMDATA, automat.paramdata, oleauto/LPPARAMDATA, oleauto/PARAMDATA"
ms.topic: struct
req.header: oleauto.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OleAuto.h
api_name:
 - PARAMDATA
product: Windows
targetos: Windows
req.typenames: PARAMDATA, *LPPARAMDATA
req.redist: 
---

# PARAMDATA structure


## -description


Describes a parameter accepted by a method or property.


## -struct-fields




### -field szName

The parameter name. Names should follow standard conventions for programming language access; that is, no embedded spaces or control characters, and 32 or fewer characters. The name should be localized because each type description provides names for a particular locale.


### -field vt

The parameter type. If more than one parameter type is accepted, VT_VARIANT should be specified.

