---
UID: NF:propvarutil.StgDeserializePropVariant
title: StgDeserializePropVariant function
author: windows-driver-content
description: Deserializes a specified SERIALIZEDPROPERTYVALUE structure, creating a PROPVARIANT structure.
old-location: properties\StgDeserializePropVariant.htm
old-project: properties
ms.assetid: 0517ef4d-e57c-4613-8d11-5e1eb14eb9fa
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: StgDeserializePropVariant, StgDeserializePropVariant function [Windows Properties], _shell_StgDeserializePropVariant, properties.StgDeserializePropVariant, propvarutil/StgDeserializePropVariant, shell.StgDeserializePropVariant
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
-	StgDeserializePropVariant
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# StgDeserializePropVariant function


## -description


Deserializes a specified <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a> structure, creating a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param pprop [in]

Type: <b>const <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a> structure.


### -param cbMax [in]

Type: <b>ULONG</b>

The size of the <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a> structure, in bytes.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Pointer to the resulting <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.
                


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



