---
UID: NS:shlobj_core.EXP_PROPERTYSTORAGE
title: EXP_PROPERTYSTORAGE
author: windows-sdk-content
description: Stores information about the Shell link state. This structure is used for extra data sections that are tagged with EXP_PROPERTYSTORAGE_SIG.
old-location: shell\EXP_PROPERTYSTORAGE.htm
old-project: shell
ms.assetid: b7228610-c28a-4e19-80c9-30997a360b9c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EXP_PROPERTYSTORAGE, EXP_PROPERTYSTORAGE structure [Windows Shell], _shell_EXP_PROPERTYSTORAGE, shell.EXP_PROPERTYSTORAGE, shlobj_core/EXP_PROPERTYSTORAGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: EXP_PROPERTYSTORAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - EXP_PROPERTYSTORAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# EXP_PROPERTYSTORAGE structure


## -description


Stores information about the Shell link state. This structure is used for extra data sections that are tagged with EXP_PROPERTYSTORAGE_SIG.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field dwSignature

Type: <b>DWORD</b>

Identifies the type of block and is the value EXP_PROPERTYSTORAGE_SIG.


### -field abPropertyStorage

Type: <b>BYTE[1]</b>

A serialized property store in the format defined by SERIALIZEDPROPSTORAGE.


## -remarks



 EXP_PROPERTYSTORAGE is used to store information serialized by the <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> object.  It is named with the tag value EXP_PROPERTYSTORAGE_SIG and can be accessed via <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>, including operations for add, remove, and copy. This block can be used to inspect the Shell link state.



