---
UID: NS:shlobj_core.EXP_DARWIN_LINK
title: EXP_DARWIN_LINK
author: windows-sdk-content
description: Holds an extra data block used by IShellLinkDataList. It holds the link's Windows Installer ID.
old-location: shell\EXP_DARWIN_LINK_str.htm
old-project: shell
ms.assetid: 016c539e-6035-4752-99b6-71e2d7199bf0
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPEXP_DARWIN_LINK, EXP_DARWIN_ID_SIG, EXP_DARWIN_LINK, EXP_DARWIN_LINK structure [Windows Shell], LPEXP_DARWIN_LINK, LPEXP_DARWIN_LINK structure pointer [Windows Shell], _win32_EXP_DARWIN_LINK_str, shell.EXP_DARWIN_LINK_str, shlobj_core/EXP_DARWIN_LINK, shlobj_core/LPEXP_DARWIN_LINK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
tech.root: 
req.typenames: EXP_DARWIN_LINK, *LPEXP_DARWIN_LINK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	EXP_DARWIN_LINK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# EXP_DARWIN_LINK structure


## -description


Holds an extra data block used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>. It holds the link's Windows Installer ID.


## -struct-fields




### -field dbh

Type: <b><a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a></b>


<a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a> structure stating the size and signature of the <b>EXP_DARWIN_LINK</b> structure. The following is the only recognized signature value.



#### EXP_DARWIN_ID_SIG

The <b>EXP_DARWIN_LINK</b> structure contains a Windows Installer ID.


### -field DUMMYSTRUCTNAME

 


### -field szDarwinID

Type: <b>__wchar_t[MAX_PATH]</b>

The link's ID in the form of an ANSI string.


### -field szwDarwinID

Type: <b>WCHAR[MAX_PATH]</b>

The link's ID in the form of an Unicode string.


## -remarks




<a href="https://msdn.microsoft.com/d6ebfd84-6ef4-43be-af16-71fc395c4735">IShellLinkDataList::GetFlags</a> returns the flag SLDF_HAS_DARWINID for links that have a darwin signature.




## -see-also




<a href="https://msdn.microsoft.com/d6ebfd84-6ef4-43be-af16-71fc395c4735">IShellLinkDataList::GetFlags</a>
 

 

