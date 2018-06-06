---
UID: NF:intsafe.UShortToUInt8
title: UShortToUInt8 function
author: windows-sdk-content
description: Converts a value of type USHORT to a value of type UINT8.
old-location: shell\UShortToUInt8.htm
old-project: shell
ms.assetid: 86e8a064-ce83-4224-81d3-84db39905f34
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UShortToByte, UShortToUInt8, UShortToUInt8 function [Windows Shell], WordToByte, intsafe/UShortToUInt8, shell.UShortToUInt8
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - UShortToUInt8
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




## -remarks



<b>WordToByte</b> is an alias for this function.

<b>UShortToByte</b> is an alias for this function.



