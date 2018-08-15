---
UID: NF:intsafe.ShortToDWordPtr
title: ShortToDWordPtr function
author: windows-sdk-content
description: Converts a value of type SHORT to a value of type DWORD_PTR.
old-location: shell\ShortToDWordPtr.htm
old-project: shell
ms.assetid: e5d0bb74-adde-48c7-b2df-1ba86d528db1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ShortToDWordPtr, ShortToDWordPtr function [Windows Shell], intsafe/ShortToDWordPtr, shell.ShortToDWordPtr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.redist: 
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
 - ShortToDWordPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToDWordPtr function


## -description


Converts a value of type <b>SHORT</b> to a value of type <b>DWORD_PTR</b>.


## -parameters




### -param sOperand [in]

The value to convert.


### -param pdwResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



