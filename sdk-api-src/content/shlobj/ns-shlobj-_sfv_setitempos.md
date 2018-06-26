---
UID: NS:shlobj._SFV_SETITEMPOS
title: "_SFV_SETITEMPOS"
author: windows-sdk-content
description: Stores position information for an item. Used with message SFVM_SETITEMPOS.
old-location: shell\SFV_SETITEMPOS.htm
old-project: shell
ms.assetid: 5ee6ef2b-2d06-42ec-b70e-659c2f137714
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: "*LPSFV_SETITEMPOS, SFV_SETITEMPOS, SFV_SETITEMPOS structure [Windows Shell], _SFV_SETITEMPOS, _shell_SFV_SETITEMPOS, shell.SFV_SETITEMPOS, shlobj/SFV_SETITEMPOS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SFV_SETITEMPOS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shlobj.h
api_name:
 - SFV_SETITEMPOS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _SFV_SETITEMPOS structure


## -description


Stores position information for an item. Used with message <a href="https://msdn.microsoft.com/b89f2d62-095b-4cad-a47e-2d41e122cb3e">SFVM_SETITEMPOS</a>.


## -struct-fields




### -field pidl

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> for the item.


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure indicating the position of the item.

