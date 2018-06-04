---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# FNFCIGETTEMPFILE macro


## -description


The <b>FNFCIGETTEMPFILE</b> macro provides the declaration for the application-defined callback function to obtain a temporary file name.


## -parameters




### -param fn

TBD






#### - cbTempName [in]

 Size, in bytes, of the <i>pszTempName</i> buffer.


#### - pszTempName [out]

Pointer to a buffer to receive the complete temporary file name.


#### - pv

Pointer to an application-defined value.


## -remarks



The function can return a filename that already exists by the time it is opened. For this reason, the caller should be prepared to make several attempts to create temporary files.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>FNFCIGETTEMPFILE(fnGetTempFileName)
{
    BOOL bSucceeded = FALSE;
    CHAR pszTempPath[MAX_PATH];
    CHAR pszTempFile[MAX_PATH];

    UNREFERENCED_PARAMETER(pv);
    UNREFERENCED_PARAMETER(cbTempName);

    if( GetTempPathA(MAX_PATH, pszTempPath) != 0 )
    {
        if( GetTempFileNameA(pszTempPath, "CABINET", 0, pszTempFile) != 0 )
        {
            DeleteFileA(pszTempFile);
            bSucceeded = SUCCEEDED(StringCbCopyA(pszTempName, cbTempName, pszTempFile));
        }
    }

    return bSucceeded;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

