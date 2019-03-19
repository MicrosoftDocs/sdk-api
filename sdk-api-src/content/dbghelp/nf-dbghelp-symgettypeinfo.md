---
UID: NF:dbghelp.SymGetTypeInfo
title: SymGetTypeInfo function (dbghelp.h)
author: windows-sdk-content
description: Retrieves type information for the specified type index.
old-location: base\symgettypeinfo.htm
tech.root: Debug
ms.assetid: bc94a5b1-d49d-425a-89a8-c584c3979930
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymGetTypeInfo, SymGetTypeInfo function, _win32_symgettypeinfo, base.symgettypeinfo, dbghelp/SymGetTypeInfo
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - imagehlp.dll
api_name:
 - SymGetTypeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymGetTypeInfo function


## -description


Retrieves type information for the specified type index. For larger queries, use the <a href="https://msdn.microsoft.com/77e0a8ad-8c75-4bb2-869a-670429475ccc">SymGetTypeInfoEx</a> function.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param ModBase [in]

The base address of the module.


### -param TypeId [in]

The type index. (A number of functions return a type index in the <b>TypeIndex</b> member of the 
<a href="https://msdn.microsoft.com/785a9702-8b77-4ce1-99df-143ce78490ab">SYMBOL_INFO</a> structure.)


### -param GetType [in]

The information type. This parameter can be one of more of the values from the <a href="https://msdn.microsoft.com/1b21c8dc-240f-4202-bd61-8f9dae0d053a">IMAGEHLP_SYMBOL_TYPE_INFO</a> enumeration type. 




### -param pInfo [out]

The data. The format of the data depends on the value of the <i>GetType</i> parameter.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



For more details on the type information, see the documentation for the PDB format.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/1b21c8dc-240f-4202-bd61-8f9dae0d053a">IMAGEHLP_SYMBOL_TYPE_INFO</a>



<a href="https://msdn.microsoft.com/3a48365f-3b8a-493d-9fd9-dde77be9ced2">SymGetTypeFromName</a>



<a href="https://msdn.microsoft.com/77e0a8ad-8c75-4bb2-869a-670429475ccc">SymGetTypeInfoEx</a>
 

 

