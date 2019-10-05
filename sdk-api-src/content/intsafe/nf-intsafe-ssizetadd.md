---
UID: NF:intsafe.SSIZETAdd
title: SSIZETAdd function (intsafe.h)
author: windows-sdk-content
description: Adds two SSIZE_T values together.
old-location: shell\SSIZETAdd.htm
tech.root: shell
ms.assetid: a9a2eb36-f70b-45fb-a84a-391a0bb77954
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SSIZETAdd, SSIZETAdd function [Windows Shell], intsafe/SSIZETAdd, shell.SSIZETAdd
ms.topic: function
f1_keywords: 
 - "intsafe/SSIZETAdd"
dev_langs:
 - c++
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
 - SSIZETAdd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SSIZETAdd function


## -description


Adds two SSIZE_T values together.


## -parameters




### -param Augend [in]

The value to add to <i>Addend</i>.


### -param Addend [in]

The value to be added to <i>Augend</i>.


### -param pResult [out]

When this function returns successfully, points to the sum of <i>Augend</i> plus <i>Addend</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



