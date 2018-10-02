---
UID: NF:intsafe.ULongLongToUInt8
title: ULongLongToUInt8 function
author: windows-sdk-content
description: Converts a value of type ULONGLONG to a value of type UINT8.
old-location: shell\ULongLongToUInt8.htm
tech.root: Shell
ms.assetid: 7aec4c8f-c2fc-4e57-bc27-b5b853fbd2ab
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ULongLongToUInt8, ULongLongToUInt8 function [Windows Shell], intsafe/ULongLongToUInt8, shell.ULongLongToUInt8
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - ULongLongToUInt8
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ULongLongToUInt8 function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>UINT8</b>.


## -parameters




### -param ullOperand [in]

The value to convert.


### -param pu8Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



