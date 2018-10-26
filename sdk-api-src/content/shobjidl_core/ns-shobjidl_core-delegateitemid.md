---
UID: NS:shobjidl_core.DELEGATEITEMID
title: DELEGATEITEMID
author: windows-sdk-content
description: Used by delegate folders in place of a standard ITEMIDLIST structure.
old-location: shell\DELEGATEITEMID.htm
tech.root: shell
ms.assetid: 986591cf-97c5-4328-900e-b49f0f0859a5
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PDELEGATEITEMID, DELEGATEITEMID, DELEGATEITEMID structure [Windows Shell], shell.DELEGATEITEMID, shell_DELEGATEITEMID, shobjidl_core/DELEGATEITEMID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - DELEGATEITEMID
product: Windows
targetos: Windows
req.typenames: DELEGATEITEMID
req.redist: 
---

# DELEGATEITEMID structure


## -description


Used by delegate folders in place of a standard <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


## -struct-fields




### -field cbSize

Type: <b>WORD</b>

The size, in bytes, of this structure.


### -field wOuter

Type: <b>WORD</b>

Private data owned by the delegating (outer) folder.


### -field cbInner

Type: <b>WORD</b>

The size, in bytes, of the delegate's data. The first <b>cbInner</b> bytes of the <b>rgb</b> array contain this data. The remaining data in <b>rgb</b> belongs to the outer folder.


### -field rgb

Type: <b>BYTE[1]</b>

An array holding the inner folder's data, which is opaque to the outer folder, followed by outer folder's data.

