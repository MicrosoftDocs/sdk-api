---
UID: NS:wabdefs._SBinaryArray
title: "_SBinaryArray"
author: windows-sdk-content
description: Do not use. An array of entry identifiers representing MAPI objects. Uses the same implementation as SBinaryArray.
old-location: wab\_wab_ENTRYLIST.htm
old-project: wab
ms.assetid: VS|wab|~\wab\reference\structures\entrylist.htm
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*LPENTRYLIST, ENTRYLIST, ENTRYLIST structure [Windows Address Book], LPENTRYLIST, LPENTRYLIST structure pointer [Windows Address Book], SBinaryArray, _SBinaryArray, _wab_ENTRYLIST, wab._wab_ENTRYLIST, wabdefs/ENTRYLIST, wabdefs/LPENTRYLIST"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: SBinaryArray
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wabdefs.h
api_name:
-	ENTRYLIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# _SBinaryArray structure


## -description


Do not use. An array of entry identifiers representing MAPI objects. Uses the same implementation as <a href="31fc6e1b-c2c1-4e74-a760-957a60005d1e">SBinaryArray</a>.


## -struct-fields




### -field cValues

Type: <b>ULONG</b>

Variable of type <b>ULONG</b> that specifies the number of entry identifiers.


### -field lpbin

Type: <b><a href="7710f883-e168-4c49-8f29-d18792b80ad4">SBinary</a>*</b>

Array of variables of type <a href="7710f883-e168-4c49-8f29-d18792b80ad4">SBinary</a> that specify the entry identifiers.

