---
UID: NF:intsafe.Int8ToUIntPtr
title: Int8ToUIntPtr function
author: windows-sdk-content
description: Converts a value of type INT8 to a value of type UINT_PTR.
old-location: shell\Int8ToUIntPtr.htm
old-project: shell
ms.assetid: 9b40adbe-c1df-4abd-b76e-839c04562d3d
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Int8ToUIntPtr, Int8ToUIntPtr function [Windows Shell], intsafe/Int8ToUIntPtr, shell.Int8ToUIntPtr
ms.prod: windows
ms.technology: windows-sdk
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
 - Int8ToUIntPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Int8ToUIntPtr function


## -description


Converts a value of type <b>INT8</b> to a value of type <b>UINT_PTR</b>.


## -parameters




### -param i8Operand [in]

The value to convert.


### -param puResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



