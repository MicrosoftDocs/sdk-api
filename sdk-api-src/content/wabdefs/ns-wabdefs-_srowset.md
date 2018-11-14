---
UID: NS:wabdefs._SRowSet
title: "_SRowSet"
author: windows-sdk-content
description: Do not use. Contains an array of SRow structures. Each SRow structure describes a row from a table.
old-location: wab\_wab_SRowSet.htm
tech.root: wab
ms.assetid: VS|wab|~\wab\reference\structures\srowset.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSRowSet, SRowSet, SRowSet structure [Windows Address Book], _SRowSet, _wab_SRowSet, wab._wab_SRowSet, wabdefs/SRowSet"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wabdefs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wabdefs.h
api_name:
 - SRowSet
product: Windows
targetos: Windows
req.typenames: SRowSet, *LPSRowSet
req.redist: 
req.product: Internet Explorer 4.0
---

# _SRowSet structure


## -description


Do not use. Contains an array of <a href="https://msdn.microsoft.com/en-us/library/ms629452(v=VS.85).aspx">SRow</a> structures. Each <b>SRow</b> structure describes a row from a table.


## -struct-fields




### -field cRows

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of <a href="https://msdn.microsoft.com/en-us/library/ms629452(v=VS.85).aspx">SRow</a> structures in the <b>aRow</b> member.


### -field aRow

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms629452(v=VS.85).aspx">SRow</a>[MAPI_DIM]</b>

Array of variables of type <a href="https://msdn.microsoft.com/en-us/library/ms629452(v=VS.85).aspx">SRow</a> that specifies the structures that represent the rows in the table. 

