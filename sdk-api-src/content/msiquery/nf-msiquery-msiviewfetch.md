---
UID: NF:msiquery.MsiViewFetch
title: MsiViewFetch function (msiquery.h)
description: The MsiViewFetch function fetches the next sequential record from the view. This function returns a handle that should be closed using MsiCloseHandle.
helpviewer_keywords: ["MsiViewFetch","MsiViewFetch function","_msi_msiviewfetch","msiquery/MsiViewFetch","setup.msiviewfetch"]
old-location: setup\msiviewfetch.htm
tech.root: setup
ms.assetid: 1a973a22-ca3a-4980-9b20-d3c5b43fdd19
ms.date: 12/05/2018
ms.keywords: MsiViewFetch, MsiViewFetch function, _msi_msiviewfetch, msiquery/MsiViewFetch, setup.msiviewfetch
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiViewFetch
 - msiquery/MsiViewFetch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiViewFetch
---

# MsiViewFetch function


## -description

The 
<b>MsiViewFetch</b> function fetches the next sequential record from the view. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

## -parameters

### -param hView [in]

Handle to the view to fetch from.

### -param phRecord [out]

Pointer to the handle for the fetched record.

## -returns

Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.

## -remarks

If the 
<b>MsiViewFetch</b> function returns ERROR_FUNCTION_FAILED, it is possible that the 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewexecute">MsiViewExecute</a> function was not called first. If more rows are available in the result set, 
<b>MsiViewFetch</b> returns <i>phRecord</i> as a handle to a record containing the requested column data, or <i>phRecord</i> is 0. For maximum performance, the same record should be used for all retrievals, or the record should be released by going out of scope.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>



<a href="/windows/desktop/Msi/working-with-queries">Working with Queries</a>