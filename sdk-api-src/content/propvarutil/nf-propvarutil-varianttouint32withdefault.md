---
UID: NF:propvarutil.VariantToUInt32WithDefault
title: VariantToUInt32WithDefault function
author: windows-sdk-content
description: Extracts an unsigned Int32 property value of a variant structure. If no value currently exists, then the specified default value is returned.
old-location: properties\VariantToUInt32WithDefault.htm
tech.root: properties
ms.assetid: 02ec869b-154e-436a-a9b7-57eff4e958aa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VariantToUInt32WithDefault, VariantToUInt32WithDefault function [Windows Properties], _shell_VariantToUInt32WithDefault, properties.VariantToUInt32WithDefault, propvarutil/VariantToUInt32WithDefault, shell.VariantToUInt32WithDefault
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
 - VariantToUInt32WithDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToUInt32WithDefault function


## -description


Extracts an unsigned <b>Int32</b> property value of a variant structure. If no value currently exists, then the specified default value is returned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param ulDefault [in]

Type: <b>ULONG</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>ULONG</b>

Returns extracted unsigned <b>Int32</b> value, or default.



