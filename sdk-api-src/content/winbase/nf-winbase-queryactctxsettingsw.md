---
UID: NF:winbase.QueryActCtxSettingsW
title: QueryActCtxSettingsW function (winbase.h)
description: The QueryActCtxSettingsW function specifies the activation context, and the namespace and name of the attribute that is to be queried.
helpviewer_keywords: ["QueryActCtxSettingsW","QueryActCtxSettingsW function [Side-by-side Assemblies]","setup.queryactctxsettingsw","winbase/QueryActCtxSettingsW"]
old-location: setup\queryactctxsettingsw.htm
tech.root: setup
ms.assetid: 80e419a5-7b57-488a-90bc-1d38d063b1ee
ms.date: 12/05/2018
ms.keywords: QueryActCtxSettingsW, QueryActCtxSettingsW function [Side-by-side Assemblies], setup.queryactctxsettingsw, winbase/QueryActCtxSettingsW
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QueryActCtxSettingsW
 - winbase/QueryActCtxSettingsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-sidebyside-l1-1-0.dll
 - KernelBase.dll
api_name:
 - QueryActCtxSettingsW
---

# QueryActCtxSettingsW function


## -description

The <b>QueryActCtxSettingsW</b> function specifies the activation context, and the namespace and name of the attribute that is to be queried.

## -parameters

### -param dwFlags [in, optional]

This value must be 0.

### -param hActCtx [in, optional]

A handle to the activation context that is being queried.

### -param settingsNameSpace [in, optional]

A pointer to a string that contains the value <b>"http://schemas.microsoft.com/SMI/2005/WindowsSettings"</b> or <b>NULL</b>. These values are equivalent.


<b>Windows 8 and Windows Server 2012:  </b>A pointer to a string that contains the value <b>"http://schemas.microsoft.com/SMI/2011/WindowsSettings"</b> is also a valid parameter.  A <b>NULL</b> is still equivalent to the previous value.

### -param settingName [in]

The name of the attribute to be queried.

### -param pvBuffer [out]

A pointer to the buffer that receives the query result.

### -param dwBuffer [in]

The size of the buffer  in characters that receives the query result.

### -param pdwWrittenOrRequired [out, optional]

A pointer to a value which is the number of characters written to the buffer specified by <i>pvBuffer</i> or that is required to hold the query result.

## -returns

If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
<a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.