---
UID: NS:shlobj._SFV_SETITEMPOS
title: SFV_SETITEMPOS (shlobj.h)
author: windows-sdk-content
description: Stores position information for an item. Used with message SFVM_SETITEMPOS.
old-location: shell\SFV_SETITEMPOS.htm
tech.root: shell
ms.assetid: 5ee6ef2b-2d06-42ec-b70e-659c2f137714
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSFV_SETITEMPOS, SFV_SETITEMPOS, SFV_SETITEMPOS structure [Windows Shell], _shell_SFV_SETITEMPOS, shell.SFV_SETITEMPOS, shlobj/SFV_SETITEMPOS"
ms.topic: struct
f1_keywords: ["shlobj/SFV_SETITEMPOS"]
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: SFV_SETITEMPOS
req.redist: 
ms.custom: 19H1
---

# SFV_SETITEMPOS structure


## -description


Stores position information for an item. Used with message <a href="https://docs.microsoft.com/windows/desktop/shell/sfvm-setitempos">SFVM_SETITEMPOS</a>.


## -struct-fields




### -field pidl

Type: <b>PCUITEMID_CHILD</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a> for the item.


### -field pt

Type: <b><a href="https://docs.microsoft.com/previous-versions//dd162805(v=vs.85)">POINT</a></b>

A <a href="https://docs.microsoft.com/previous-versions//dd162805(v=vs.85)">POINT</a> structure indicating the position of the item.

