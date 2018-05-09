---
UID: NF:shlobj_core.ILIsAligned
title: ILIsAligned function
author: windows-driver-content
description: Verifies whether a constant ITEMIDLIST is aligned on a pointer boundary, which is a DWORD on 32-bit architectures and a QWORD on 64-bit architectures.
old-location: shell\ILIsAligned.htm
old-project: shell
ms.assetid: ef6607c6-3ea0-4b45-b443-dbd1359ab873
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ILIsAligned, ILIsAligned function [Windows Shell], _shell_ILIsAligned, shell.ILIsAligned, shlobj_core/ILIsAligned
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	ILIsAligned
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# ILIsAligned function


## -description


Verifies whether a constant <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> is aligned on a pointer boundary, which is a <b>DWORD</b> on 32-bit architectures and a <b>QWORD</b> on 64-bit architectures.


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A constant PIDL relative to a parent folder that is being checked for alignment.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if aligned; otherwise, <b>FALSE</b>.




## -remarks



For use where STRICT_TYPED_ITEMIDS is defined.



