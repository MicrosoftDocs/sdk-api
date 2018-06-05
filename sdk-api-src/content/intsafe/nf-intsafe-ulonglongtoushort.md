---
UID: NF:intsafe.ULongLongToUShort
title: ULongLongToUShort function
author: windows-sdk-content
description: Converts a value of type ULONGLONG to a value of type USHORT.
old-location: shell\ULongLongToUShort.htm
old-project: shell
ms.assetid: 7e320c61-31af-485d-a023-dc656798c73a
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ULongLongToUShort, ULongLongToUShort function [Windows Shell], intsafe/ULongLongToUShort, shell.ULongLongToUShort
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	intsafe.h
api_name:
-	ULongLongToUShort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongToUShort function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>USHORT</b>.


## -parameters




### -param ullOperand [in]

The value to convert.


### -param pusResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



