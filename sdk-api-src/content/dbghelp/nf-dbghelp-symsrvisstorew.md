---
UID: NF:dbghelp.SymSrvIsStoreW
title: SymSrvIsStoreW function (dbghelp.h)
description: The SymSrvIsStoreW (Unicode) function (dbghelp.h) determines whether the specified path points to a symbol store.
helpviewer_keywords: ["SymSrvIsStore","SymSrvIsStore function","SymSrvIsStoreW","base.symsrvisstore","dbghelp/SymSrvIsStore","dbghelp/SymSrvIsStoreW"]
old-location: base\symsrvisstore.htm
tech.root: Debug
ms.assetid: 7fbec886-c1b7-4d17-9813-af7812b4abb9
ms.date: 08/04/2022
ms.keywords: SymSrvIsStore, SymSrvIsStore function, SymSrvIsStoreW, base.symsrvisstore, dbghelp/SymSrvIsStore, dbghelp/SymSrvIsStoreW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvIsStoreW (Unicode) and SymSrvIsStore (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - SymSrvIsStoreW
 - dbghelp/SymSrvIsStoreW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymSrvIsStore
 - SymSrvIsStore
 - SymSrvIsStoreW
---

# SymSrvIsStoreW function


## -description

Determines whether the specified path points to a symbol store.

## -parameters

### -param hProcess [in, optional]

The handle of a process that you previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function. If this parameter is set to  <b>NULL</b>, the function determines only whether the store exists; otherwise, the function determines whether the store exists and contains a process entry for the specified process handle.

### -param path [in]

The path to a symbol store. The path can specify the default symbol store (for example, SRV*), point to an HTTP or HTTPS symbol server, or specify a UNC, absolute, or relative path to the store.

## -returns

If the path specifies a symbol store, the function returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

If the path points to the default symbol store (for example, SRV*) or to an HTTP or HTTPS symbol server, the function assumes the store exists.

If there is a proxy computer between the client computer and the server, the version of the SymSrv.dll on the proxy cannot be less than the version that is on the client.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSrvIsStore as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
