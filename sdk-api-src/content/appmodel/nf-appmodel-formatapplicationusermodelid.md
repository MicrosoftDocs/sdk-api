---
UID: NF:appmodel.FormatApplicationUserModelId
title: FormatApplicationUserModelId function (appmodel.h)
description: Constructs an application user model ID from the package family name and the package relative application ID (PRAID).
helpviewer_keywords: ["FormatApplicationUserModelId","FormatApplicationUserModelId function [App packaging and management]","appmodel/FormatApplicationUserModelId","appxpkg.formatapplicationusermodelid"]
old-location: appxpkg\formatapplicationusermodelid.htm
tech.root: appxpkg
ms.assetid: F48D19C2-6373-41FC-A99D-E3CCB68D6C6C
ms.date: 12/05/2018
ms.keywords: FormatApplicationUserModelId, FormatApplicationUserModelId function [App packaging and management], appmodel/FormatApplicationUserModelId, appxpkg.formatapplicationusermodelid
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - FormatApplicationUserModelId
 - appmodel/FormatApplicationUserModelId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - api-ms-win-appmodel-runtime-l1-1-4.dll
 - api-ms-win-appmodel-runtime-l1-1-3.dll
 - Kernel32.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Kernel.AppCore.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - FormatApplicationUserModelId
---

# FormatApplicationUserModelId function


## -description

Constructs an <a href="/windows/desktop/appxpkg/appx-packaging-glossary">application user model ID</a> from the <i>package family name</i> and the <i>package relative application ID</i> (PRAID).

## -parameters

### -param packageFamilyName [in]

Type: <b>PCWSTR</b>

The package family name.

### -param packageRelativeApplicationId [in]

Type: <b>PCWSTR</b>

The package-relative app ID (PRAID).

### -param applicationUserModelIdLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters (<b>WCHAR</b>s) in the app user model ID string, which includes the null-terminator. 

First you pass <b>NULL</b> to <i>applicationUserModelId</i> to get the number of characters. You use this number to allocate memory space for <i>applicationUserModelId</i>. Then you pass the address of this memory space to fill <i>applicationUserModelId</i>.

### -param applicationUserModelId [out, optional]

Type: <b>PWSTR</b>

A pointer to memory space that receives  the app user model ID string, which includes the null-terminator.

## -returns

Type: <b>LONG</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>packageFamilyName</i> or <i>packageRelativeApplicationId</i> parameter isn't valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>applicationUserModelId</i> is not large enough to hold the data; the required buffer size, in <b>WCHAR</b>s, is stored in the variable pointed to by <i>applicationUserModelIdLength</i>.

</td>
</tr>
</table>