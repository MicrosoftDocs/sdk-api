---
UID: NF:fci.FNFCIOPEN
title: FNFCIOPEN macro
author: windows-sdk-content
description: The FNFCIOPEN macro provides the declaration for the application-defined callback function to open a file in an FCI context.
old-location: winprog\fnfciopen.htm
old-project: DevNotes
ms.assetid: 72cf50cb-c895-4953-9c4d-f8ddaa294f2a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FNFCIOPEN, FNFCIOPEN macro [Windows API], fci/FNFCIOPEN, winprog.fnfciopen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: fci.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fci.h
api_name:
 - FNFCIOPEN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FNFCIOPEN macro


## -description


The <b>FNFCIOPEN</b> macro provides the declaration for the application-defined callback function to open a file in an FCI context.


## -parameters




### -param fn [in]

The name of the file.


#### - err

Pointer to the error code value. 

This value will be used to provide extended error information in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FCI context.


#### - oflag

Specifies the type of operations allowed.


#### - pmode

Specifies the permission mode.


#### - pv

Pointer to an application-defined value.


## -remarks



The function accepts parameters similar to <a href="http://go.microsoft.com/fwlink/p/?linkid=196548">_open</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIOPEN(fnFileOpen)
{
    HANDLE hFile = NULL;
    DWORD dwDesiredAccess = 0; 
    DWORD dwCreationDisposition = 0;

    UNREFERENCED_PARAMETER(pv);
    UNREFERENCED_PARAMETER(pmode);

    if ( oflag &amp; _O_RDWR )
    {
        dwDesiredAccess = GENERIC_READ | GENERIC_WRITE;
    }
    else if ( oflag &amp; _O_WRONLY )
    {
        dwDesiredAccess = GENERIC_WRITE;
    }
    else
    {
        dwDesiredAccess = GENERIC_READ;
    }

    if ( oflag &amp; _O_CREAT )
    {
        dwCreationDisposition = CREATE_ALWAYS;
    }
    else
    {
        dwCreationDisposition = OPEN_EXISTING;
    }

    hFile = CreateFileA(pszFile, 
                        dwDesiredAccess,
                        FILE_SHARE_READ,
                        NULL,
                        dwCreationDisposition,
                        FILE_ATTRIBUTE_NORMAL,
                        NULL);

    if ( hFile == INVALID_HANDLE_VALUE )
    {
        *err = GetLastError();
    }

    return (INT_PTR)hFile;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

