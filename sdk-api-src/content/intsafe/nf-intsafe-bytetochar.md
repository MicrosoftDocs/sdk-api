---
UID: NF:intsafe.ByteToChar
title: ByteToChar function
author: windows-sdk-content
description: Converts a value of type BYTE to a value of type CHAR.
old-location: shell\ByteToChar.htm
tech.root: Shell
ms.assetid: d10b3450-3dfc-4acf-9853-f7c191041b33
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ByteToChar, ByteToChar function [Windows Shell], intsafe/ByteToChar, shell.ByteToChar
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
 - ByteToChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ByteToChar function


## -description


Converts a value of type <b>BYTE</b> to a value of type <b>CHAR</b>.


## -parameters




### -param bOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



