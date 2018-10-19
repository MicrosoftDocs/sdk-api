---
UID: NF:propvarutil.VariantToUInt64WithDefault
title: VariantToUInt64WithDefault function
author: windows-sdk-content
description: Extracts an unsigned Int64 property value of a variant structure. If no value currently exists, then the specified default value is returned.
old-location: properties\VariantToUInt64WithDefault.htm
tech.root: properties
ms.assetid: 6ff75c81-519b-4539-9aa5-c6b39b3e2d94
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: VariantToUInt64WithDefault, VariantToUInt64WithDefault function [Windows Properties], _shell_VariantToUInt64WithDefault, properties.VariantToUInt64WithDefault, propvarutil/VariantToUInt64WithDefault, shell.VariantToUInt64WithDefault
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToUInt64WithDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToUInt64WithDefault function


## -description


Extracts an unsigned <b>Int64</b> property value of a variant structure. If no value currently exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param ullDefault [in]

Type: <b>ULONGLONG</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>ULONGLONG</b>

Returns the extracted unsigned <b>Int64</b> value, or a default.



