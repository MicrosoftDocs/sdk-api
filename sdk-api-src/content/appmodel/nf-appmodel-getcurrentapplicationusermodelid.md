---
UID: NF:appmodel.GetCurrentApplicationUserModelId
title: GetCurrentApplicationUserModelId function (appmodel.h)
description: Gets the application user model ID for the current process.
helpviewer_keywords: ["GetCurrentApplicationUserModelId","GetCurrentApplicationUserModelId function [App packaging and management]","appmodel/GetCurrentApplicationUserModelId","appxpkg.getcurrentapplicationusermodelid"]
old-location: appxpkg\getcurrentapplicationusermodelid.htm
tech.root: appxpkg
ms.assetid: 562BB225-0922-4FE7-92C0-573A2CCE3195
ms.date: 12/05/2018
ms.keywords: GetCurrentApplicationUserModelId, GetCurrentApplicationUserModelId function [App packaging and management], appmodel/GetCurrentApplicationUserModelId, appxpkg.getcurrentapplicationusermodelid
req.header: appmodel.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentApplicationUserModelId
 - appmodel/GetCurrentApplicationUserModelId
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
 - API-MS-Win-AppModel-Runtime-l1-1-0.dll
 - kernel32legacy.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetCurrentApplicationUserModelId
---

# GetCurrentApplicationUserModelId function


## -description

Gets the <a href="/windows/desktop/appxpkg/appx-packaging-glossary">application user model ID</a> for the current process.

## -parameters

### -param applicationUserModelIdLength [in, out]

On input, the size of the  <i>applicationUserModelId</i> buffer, in wide characters. On success, the size of the buffer used, including the null terminator.

### -param applicationUserModelId [out]

A pointer to a buffer that receives the application user model ID.

## -returns

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>APPMODEL_ERROR_NO_APPLICATION</b></dt>
</dl>
</td>
<td width="60%">
The process has no application identity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by <i>applicationUserModelIdLength</i>.

</td>
</tr>
</table>

## -remarks

For info about string size limits, see <a href="/windows/desktop/appxpkg/identity-constants">Identity constants</a>.


#### Examples


```cpp
#define _UNICODE 1
#define UNICODE 1

#include <Windows.h>
#include <appmodel.h>
#include <malloc.h>
#include <stdio.h>

int __cdecl wmain()
{
    UINT32 length = 0;
    LONG rc = GetCurrentApplicationUserModelId(&length, NULL);
    if (rc != ERROR_INSUFFICIENT_BUFFER)
    {
        if (rc == APPMODEL_ERROR_NO_APPLICATION)
            wprintf(L"Desktop application\n");
        else
            wprintf(L"Error %d in GetCurrentApplicationUserModelId\n", rc);
        return 1;
    }

    PWSTR fullName = (PWSTR) malloc(length * sizeof(*fullName));
    if (fullName == NULL)
    {
        wprintf(L"Error allocating memory\n");
        return 2;
    }

    rc = GetCurrentApplicationUserModelId(&length, fullName);
    if (rc != ERROR_SUCCESS)
    {
        wprintf(L"Error %d retrieving ApplicationUserModelId\n", rc);
        return 3;
    }
    wprintf(L"%s\n", fullName);

    free(fullName);

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-getapplicationusermodelid">GetApplicationUserModelId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefullname">GetCurrentPackageFullName</a>