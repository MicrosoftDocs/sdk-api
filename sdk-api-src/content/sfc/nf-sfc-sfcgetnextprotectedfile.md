---
UID: NF:sfc.SfcGetNextProtectedFile
title: SfcGetNextProtectedFile function (sfc.h)
author: windows-sdk-content
description: Retrieves the complete list of protected files.
old-location: setup\sfcgetnextprotectedfile.htm
tech.root: wfp
ms.assetid: 122261d5-b758-4088-8c8b-64b38c6092f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SfcGetNextProtectedFile, SfcGetNextProtectedFile function [Setup API], _win32_sfcgetnextprotectedfile, setup.sfcgetnextprotectedfile, sfc/SfcGetNextProtectedFile
ms.topic: function
f1_keywords: 
 - "sfc/SfcGetNextProtectedFile"
req.header: sfc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sfc.lib
req.dll: Sfc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sfc.dll
api_name:
 - SfcGetNextProtectedFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SfcGetNextProtectedFile function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements section. Support for this function was removed in Windows Vista and Windows Server 2008. Use the supported functions listed in <a href="https://docs.microsoft.com/windows/desktop/Wfp/wfp-functions">WRP Functions</a> instead.]

Retrieves the complete list of protected files. Applications should not replace these files.


## -parameters




### -param RpcHandle [in]

This parameter must be <b>NULL</b>.


### -param ProtFileData [in, out]

The list of protected files. The format of this structure is as follows. 




<pre class="syntax" xml:space="preserve"><code>typedef struct _PROTECTED_FILE_DATA {
    WCHAR   FileName[MAX_PATH];
    DWORD   FileNumber;
} PROTECTED_FILE_DATA, *PPROTECTED_FILE_DATA;</code></pre>
Before calling this function the first time, set the <b>FileNumber</b> member to zero.


## -returns



If the function succeeds, the return value is nonzero.

If there are no more protected files to enumerate, the return value is zero and 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_MORE_FILES. If the function fails, <b>GetLastError</b> will return a different error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sfc/nf-sfc-sfcisfileprotected">SfcIsFileProtected</a>
 

 

