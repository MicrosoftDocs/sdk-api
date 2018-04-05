---
UID: NF:intsafe.UShortToUInt8
title: UShortToUInt8 function
author: windows-driver-content
description: Converts a value of type USHORT to a value of type UINT8.
old-location: shell\UShortToUInt8.htm
old-project: shell
ms.assetid: 86e8a064-ce83-4224-81d3-84db39905f34
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: UShortToUInt8, UShortToUInt8 function [Windows Shell], intsafe/UShortToUInt8, shell.UShortToUInt8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	intsafe.h
api_name:
-	UShortToUInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UShortToUInt8 function


## -description


Converts a value of type <b>USHORT</b> to a value of type <b>UINT8</b>.


## -parameters




### -param usOperand [in]

The value to convert.


### -param pui8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



