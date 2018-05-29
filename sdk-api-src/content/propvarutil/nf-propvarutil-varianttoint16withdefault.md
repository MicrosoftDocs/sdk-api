---
UID: NF:propvarutil.VariantToInt16WithDefault
title: VariantToInt16WithDefault function
author: windows-sdk-content
description: Extracts an Int16 property value of a variant structure. If no value exists, then the specified default value is returned.
old-location: properties\VariantToInt16WithDefault.htm
old-project: properties
ms.assetid: 4d6d0b7d-ae20-456c-9ef4-97fa682ece8b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: VariantToInt16WithDefault, VariantToInt16WithDefault function [Windows Properties], _shell_VariantToInt16WithDefault, properties.VariantToInt16WithDefault, propvarutil/VariantToInt16WithDefault, shell.VariantToInt16WithDefault
ms.prod: windows
ms.technology: windows-sdk
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
-	VariantToInt16WithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VariantToInt16WithDefault function


## -description


Extracts an <b>Int16</b> property value of a variant structure. If no value exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iDefault [in]

Type: <b>SHORT</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>SHORT</b>

Returns the extracted <b>Int16</b> value, or default.



