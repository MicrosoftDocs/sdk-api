---
UID: NF:propvarutil.PropVariantToInt16WithDefault
title: PropVariantToInt16WithDefault function
author: windows-sdk-content
description: Extracts the Int16 property value of a PROPVARIANT structure. If no value currently exists, then specified default value is returned.
old-location: properties\PropVariantToInt16WithDefault.htm
tech.root: properties
ms.assetid: 51221281-6e06-49f4-83c0-7330f2a6d67e
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PropVariantToInt16WithDefault, PropVariantToInt16WithDefault function [Windows Properties], properties.PropVariantToInt16WithDefault, propvarutil/PropVariantToInt16WithDefault, shell.PropVariantToInt16WithDefault, shell_PropVariantToInt16WithDefault
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
 - PropVariantToInt16WithDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToInt16WithDefault function


## -description


Extracts the Int16 property value of a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. If no value currently exists, then specified default value is returned.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param iDefault [in]

Type: <b>SHORT</b>

Specifies default property value, for use where no value currently exists.


## -returns



Type: <b>SHORT</b>

Returns the extracted <b>short</b> value, or default.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an <b>Int16</b> value and would like to use a default value if it does not. For instance, an application obtaining values from a property store can use this to safely extract the <b>SHORT</b> value for <b>Int16</b> properties.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_I2</b>, this helper function extracts the <b>Int16</b> value. Otherwise, it attempts to convert the value in the <b>PROPVARIANT</b> structure into a <b>SHORT</b>. If the source <b>PROPVARIANT</b> has type <b>VT_EMPTY</b> or a conversion is not possible, then <a href="shell.PropVariantToInt16WithDefault">PropVariantToInt16WithDefault</a> will return the default provided by <i>iDefault</i>. See <a href="shell.PropVariantChangeType">PropVariantChangeType</a> for a list of possible conversions.




## -see-also




<a href="shell.InitPropVariantFromInt16">InitPropVariantFromInt16</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToInt16">PropVariantToInt16</a>



<a href="shell.VariantToInt16">VariantToInt16</a>
 

 

