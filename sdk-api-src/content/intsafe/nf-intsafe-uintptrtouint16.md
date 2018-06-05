---
UID: NF:intsafe.UIntPtrToUInt16
title: UIntPtrToUInt16 function
author: windows-sdk-content
description: Converts a value of type UINT_PTR to a value of type UINT16.
old-location: shell\UIntPtrToUInt16.htm
old-project: shell
ms.assetid: ff01f865-5955-48a6-abcd-205488028f00
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UIntPtrToUInt16, UIntPtrToUInt16 function [Windows Shell], intsafe/UIntPtrToUInt16, shell.UIntPtrToUInt16
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
-	UIntPtrToUInt16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToUInt16 function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>UINT16</b>.


## -parameters




### -param uOperand [in]

The value to convert.


### -param pu16Result [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



