---
UID: NF:intsafe.Int8ToUInt8
title: Int8ToUInt8 function
author: windows-driver-content
description: Converts a value of type INT8 to a value of type UINT8.
old-location: shell\Int8ToUInt8.htm
old-project: shell
ms.assetid: 1638bfca-9cec-4d01-b3b0-47a4358e35d1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Int8ToUInt8, Int8ToUInt8 function [Windows Shell], intsafe/Int8ToUInt8, shell.Int8ToUInt8
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
-	Int8ToUInt8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Int8ToUInt8 function


## -description


Converts a value of type <b>INT8</b> to a value of type <b>UINT8</b>.


## -parameters




### -param i8Operand [in]

The value to convert.


### -param pu8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



