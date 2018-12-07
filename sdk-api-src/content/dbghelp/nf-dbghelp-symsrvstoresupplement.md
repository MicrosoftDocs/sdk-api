---
UID: NF:dbghelp.SymSrvStoreSupplement
title: SymSrvStoreSupplement function
author: windows-sdk-content
description: Stores a file in the specified supplement to a symbol store. The file is typically associated with a file in the symbol server.
old-location: base\symsrvstoresupplement.htm
tech.root: debug
ms.assetid: 579bd9ff-cb23-426b-8188-6897d83ada28
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymSrvStoreSupplement, SymSrvStoreSupplement function, SymSrvStoreSupplementW, base.symsrvstoresupplement, dbghelp/SymSrvStoreSupplement, dbghelp/SymSrvStoreSupplementW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvStoreSupplementW (Unicode) and SymSrvStoreSupplement (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymSrvStoreSupplement
 - SymSrvStoreSupplement
 - SymSrvStoreSupplementW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
---

# SymSrvStoreSupplement function


## -description


Stores a file in the specified supplement to a symbol store. The file is typically associated with a file in the symbol server.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param SrvPath

TBD


### -param Node [in]

The symbol file associated with the supplemental file.


### -param File [in]

The name of the file.


### -param Flags [in]

If this parameter is <b>SYMSTOREOPT_COMPRESS</b>, the file is compressed in the symbol store. Currently, there are no other supported values.


#### - SymPath [in, optional]

The path to the symbol store.


## -returns



If the function succeeds, the return value is the fully qualified path for the supplemental file.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An important use for this function is to store delta files. For more information, see <a href="https://msdn.microsoft.com/35be6aff-efc7-4ed9-bfe7-3d0f798acbd9">SymSrvDeltaName</a>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

The symbol server stores supplemental files with the same extension in a common directory. For example, Sup1.xml would be stored in the following directory: <i>SymPath</i>\supplement\<i>Node</i>\xml.

The administrator of a store can prevent users from writing supplemental files by creating a read-only file in the root of the store named Supplement. Alternatively, the administrator can create the supplement directory and use ACLs to control access.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/2cad61c6-c8a1-437f-8e2c-1fa70eb348c2">SymSrvGetSupplement</a>
 

 

