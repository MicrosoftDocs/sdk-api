---
UID: NF:appmodel.ParseApplicationUserModelId
title: ParseApplicationUserModelId function (appmodel.h)
description: Deconstructs an application user model ID to its package family name and package relative application ID (PRAID).
helpviewer_keywords: ["ParseApplicationUserModelId","ParseApplicationUserModelId function [App packaging and management]","appmodel/ParseApplicationUserModelId","appxpkg.parseapplicationusermodelid"]
old-location: appxpkg\parseapplicationusermodelid.htm
tech.root: appxpkg
ms.assetid: 03B29E82-611F-47D1-8CB6-047B9BEB4D9E
ms.date: 12/05/2018
ms.keywords: ParseApplicationUserModelId, ParseApplicationUserModelId function [App packaging and management], appmodel/ParseApplicationUserModelId, appxpkg.parseapplicationusermodelid
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
 - ParseApplicationUserModelId
 - appmodel/ParseApplicationUserModelId
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
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - ParseApplicationUserModelId
---

# ParseApplicationUserModelId function


## -description

Deconstructs an <a href="/windows/desktop/appxpkg/appx-packaging-glossary">application user model ID</a> to its <i>package family name</i> and <i>package relative application ID</i> (PRAID).

## -parameters

### -param applicationUserModelId [in]

Type: <b>PCWSTR</b>

The app user model ID.

### -param packageFamilyNameLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters (<b>WCHAR</b>s) in the package family name string, which includes the null-terminator. 

First you pass <b>NULL</b> to <i>packageFamilyName</i> to get the number of characters. You use this number to allocate memory space for <i>packageFamilyName</i>. Then you pass the address of this memory space to fill <i>packageFamilyName</i>.

### -param packageFamilyName [out, optional]

Type: <b>PWSTR</b>

A pointer to memory space that receives  the package family name string, which includes the null-terminator.

### -param packageRelativeApplicationIdLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters (<b>WCHAR</b>s) in the package-relative app ID string, which includes the null-terminator. 

First you pass <b>NULL</b> to <i>packageRelativeApplicationId</i> to get the number of characters. You use this number to allocate memory space for <i>packageRelativeApplicationId</i>. Then you pass the address of this memory space to fill <i>packageRelativeApplicationId</i>.

### -param packageRelativeApplicationId [out, optional]

Type: <b>PWSTR</b>

A pointer to memory space that receives  the package-relative app ID (PRAID) string, which includes the null-terminator.

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
The <i>applicationUserModelId</i> parameter isn't valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>packageFamilyName</i> or <i>packageRelativeApplicationId</i> is not large enough to hold the data; the required buffer size, in <b>WCHAR</b>s, is stored in the variable pointed to by <i>packageFamilyNameLength</i> or <i>packageRelativeApplicationIdLength</i>.

</td>
</tr>
</table>