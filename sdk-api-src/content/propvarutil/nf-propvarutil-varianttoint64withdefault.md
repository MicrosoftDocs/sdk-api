---
UID: NF:propvarutil.VariantToInt64WithDefault
title: VariantToInt64WithDefault function
author: windows-driver-content
description: Extracts an Int64 property value of a variant structure. If no value exists, then the specified default value is returned.
old-location: properties\VariantToInt64WithDefault.htm
old-project: properties
ms.assetid: c4a5fc5c-19f9-4313-9d98-a486bfdfb359
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: VariantToInt64WithDefault, VariantToInt64WithDefault function [Windows Properties], _shell_VariantToInt64WithDefault, properties.VariantToInt64WithDefault, propvarutil/VariantToInt64WithDefault, shell.VariantToInt64WithDefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	VariantToInt64WithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# VariantToInt64WithDefault function


## -description


Extracts an <b>Int64</b> property value of a variant structure. If no value exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param llDefault [in]

Type: <b>LONGLONG</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>LONGLONG</b>

Returns extracted <b>Int64</b> value, or default.



