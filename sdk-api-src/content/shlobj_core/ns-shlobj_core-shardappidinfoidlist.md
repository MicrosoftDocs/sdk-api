---
UID: NS:shlobj_core.SHARDAPPIDINFOIDLIST
title: SHARDAPPIDINFOIDLIST
author: windows-sdk-content
description: Contains data used by SHAddToRecentDocs to identify both an item&#8212;in this case by an absolute pointer to an item identifier list (PIDL)&#8212;and the process that it is associated with.
old-location: shell\SHARDAPPIDINFOIDLIST.htm
old-project: shell
ms.assetid: 11c69ff9-b8a0-4168-8036-f45a9f7813ba
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHARDAPPIDINFOIDLIST, SHARDAPPIDINFOIDLIST structure [Windows Shell], _shell_SHARDAPPIDINFOIDLIST, shell.SHARDAPPIDINFOIDLIST, shlobj_core/SHARDAPPIDINFOIDLIST
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SHARDAPPIDINFOIDLIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	SHARDAPPIDINFOIDLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# SHARDAPPIDINFOIDLIST structure


## -description


Contains data used by <a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a> to identify both an item—in this case by an absolute pointer to an item identifier list (PIDL)—and the process that it is associated with.


## -struct-fields




### -field pidl

Type: <b>PCIDLIST_ABSOLUTE</b>

An absolute PIDL that gives the full path of the item in the Shell namespace.


### -field pszAppID

Type: <b>PCWSTR</b>

The application-defined AppUserModelID associated with the item.


## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/bb2b7e86-04ca-4dd0-944b-a95e8a0be1e0">SHARDAPPIDINFO</a>



<a href="https://msdn.microsoft.com/01613dc9-4516-4995-bd31-feee2eb650b2">SHARDAPPIDINFOLINK</a>



<a href="https://msdn.microsoft.com/84e065e6-b68d-4303-b98b-3f8507539468">SHAddToRecentDocs</a>
 

 

