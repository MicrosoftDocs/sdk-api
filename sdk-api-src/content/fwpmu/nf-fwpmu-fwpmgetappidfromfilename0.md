---
UID: NF:fwpmu.FwpmGetAppIdFromFileName0
title: FwpmGetAppIdFromFileName0 function (fwpmu.h)
description: Retrieves an application identifier from a file name.
helpviewer_keywords: ["FwpmGetAppIdFromFileName0","FwpmGetAppIdFromFileName0 function [Filtering]","fwp.fwpmgetappidfromfilename0","fwpmu/FwpmGetAppIdFromFileName0"]
old-location: fwp\fwpmgetappidfromfilename0.htm
tech.root: fwp
ms.assetid: 9bf3a101-7782-4075-bc77-a003184d0cbe
ms.date: 12/05/2018
ms.keywords: FwpmGetAppIdFromFileName0, FwpmGetAppIdFromFileName0 function [Filtering], fwp.fwpmgetappidfromfilename0, fwpmu/FwpmGetAppIdFromFileName0
req.header: fwpmu.h
req.include-header: 
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmGetAppIdFromFileName0
 - fwpmu/FwpmGetAppIdFromFileName0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmGetAppIdFromFileName0
---

# FwpmGetAppIdFromFileName0 function


## -description

The <b>FwpmGetAppIdFromFileName0 </b> function retrieves an application identifier from a file name.

## -parameters

### -param fileName [in]

Type: <b>const wchar_t*</b>

File name from which the application identifier will be retrieved.

### -param appId [out]

Type: [FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)**</b>

The  retrieved application identifier.

## -returns

Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The application identifier  was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>

## -remarks

The caller must free the returned object by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

<b>FwpmGetAppIdFromFileName0 </b> is a specific implementation of FwpmGetAppIdFromFileName. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example shows how to retrieve an application identifier using <b>FwpmGetAppIdFromFileName0</b>.


```cpp
#include <windows.h>
#include <fwpmu.h>
#include <stdio.h>

#pragma comment(lib, "Fwpuclnt.lib")

// Hard-coded file name for demonstration purposes.
#define FILE_PATH1 L"C:\\Program Files\\SomeAppFolder\\SomeApplication.exe"


int main()
{
    DWORD  result = ERROR_SUCCESS; 
    
    FWP_BYTE_BLOB *fwpApplicationByteBlob = NULL;
     
    printf("Retrieving Id for application to allow through firewall.\n");
    result = FwpmGetAppIdFromFileName0(FILE_PATH1, &fwpApplicationByteBlob);

    if (result != ERROR_SUCCESS)
    {
        printf("FwpmGetAppIdFromFileName failed (%d).\n", result);
        return result;
    }
    else
    {
        printf("The Id is: %d\n", fwpApplicationByteBlob->data);
    }
    
    return 0;
}
// ----------------------------------------------------------------------


```

## -see-also

[FWP_BYTE_BLOB](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)