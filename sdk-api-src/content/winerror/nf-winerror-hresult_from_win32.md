---
UID: NF:winerror.HRESULT_FROM_WIN32
title: HRESULT_FROM_WIN32 macro
author: windows-sdk-content
description: Maps a system error code to an HRESULT value.
old-location: com\hresult_from_win32_macro.htm
tech.root: com
ms.assetid: 40e6f80d-a778-4d5f-bb1b-db294815f8b5
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: HRESULT_FROM_WIN32, HRESULT_FROM_WIN32 macro [COM], _com_HRESULT_FROM_WIN32, com.hresult_from_win32, com.hresult_from_win32_macro, winerror/HRESULT_FROM_WIN32
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winerror.h
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
 - Winerror.h
api_name:
 - HRESULT_FROM_WIN32
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HRESULT_FROM_WIN32 macro


## -description


Maps a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a> to an <b>HRESULT</b> value. 


## -parameters




### -param x

The system error code.


## -remarks



This macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>//
// HRESULT_FROM_WIN32(x) used to be a macro, however we now run it as an inline function
// to prevent double evaluation of 'x'. If you still need the macro, you can use __HRESULT_FROM_WIN32(x)
//
#define __HRESULT_FROM_WIN32(x) ((HRESULT)(x) &lt;= 0 ? ((HRESULT)(x)) : ((HRESULT) (((x) &amp; 0x0000FFFF) | (FACILITY_WIN32 &lt;&lt; 16) | 0x80000000)))

#ifndef __midl
FORCEINLINE HRESULT HRESULT_FROM_WIN32(unsigned long x) { 
   return (HRESULT)(x) &lt;= 0 ? (HRESULT)(x) : (HRESULT) (((x) &amp; 0x0000FFFF) | (FACILITY_WIN32 &lt;&lt; 16) | 0x80000000);
}
#else
#define HRESULT_FROM_WIN32(x) __HRESULT_FROM_WIN32(x)
#endif

</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling</a>
 

 

