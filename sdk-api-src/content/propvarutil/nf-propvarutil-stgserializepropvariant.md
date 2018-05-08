---
UID: NF:propvarutil.StgSerializePropVariant
title: StgSerializePropVariant function
author: windows-driver-content
description: Serializes a specified PROPVARIANT structure, creating a SERIALIZEDPROPERTYVALUE structure.
old-location: properties\StgSerializePropVariant.htm
old-project: properties
ms.assetid: c588e239-616f-4569-88b5-6bfb504cefa1
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: StgSerializePropVariant, StgSerializePropVariant function [Windows Properties], _shell_StgSerializePropVariant, properties.StgSerializePropVariant, propvarutil/StgSerializePropVariant, shell.StgSerializePropVariant
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
-	StgSerializePropVariant
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# StgSerializePropVariant function


## -description


Serializes a specified <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure, creating a <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a> structure.


## -parameters




### -param ppropvar [in]

Type: <b>const <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A constant pointer to the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param ppProp [out]

Type: <b><a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a>**</b>

The address of a pointer to the <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a> structure.


### -param pcb [out]

Type: <b>ULONG*</b>

                  A pointer to the value representing the size of the <a href="https://msdn.microsoft.com/ab64a16e-624d-427a-8f9c-5c8c4a9df625">SERIALIZEDPROPERTYVALUE</a> structure.
                


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



