---
UID: NF:propvarutil.VariantToInt32WithDefault
title: VariantToInt32WithDefault function
author: windows-sdk-content
description: Extracts an Int32 property value of a variant structure. If no value exists, then the specified default value is returned.
old-location: properties\VariantToInt32WithDefault.htm
old-project: properties
ms.assetid: fd2d5330-2b31-4dbb-b57b-4ca5579fa03f
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: VariantToInt32WithDefault, VariantToInt32WithDefault function [Windows Properties], _shell_VariantToInt32WithDefault, properties.VariantToInt32WithDefault, propvarutil/VariantToInt32WithDefault, shell.VariantToInt32WithDefault
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToInt32WithDefault
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# VariantToInt32WithDefault function


## -description


Extracts an <b>Int32</b> property value of a variant structure. If no value exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param lDefault [in]

Type: <b>LONG</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>LONG</b>

Returns the extracted Int32 value, or default.



