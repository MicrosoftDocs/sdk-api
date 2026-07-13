---
UID: NF:sysinfoapi.InstallELAMCertificateInfo
title: InstallELAMCertificateInfo function (sysinfoapi.h)
description: Installs the certificate information specified in the resource file, which is linked into the ELAM driver at build time.
helpviewer_keywords: ["InstallELAMCertificateInfo","InstallELAMCertificateInfo function","base.installelamcertificateinfo","sysinfoapi/InstallELAMCertificateInfo"]
old-location: base\installelamcertificateinfo.htm
tech.root: security
ms.assetid: 0EF40169-A078-4B1E-96EC-5390C75639F8
ms.date: 12/05/2018
ms.keywords: InstallELAMCertificateInfo, InstallELAMCertificateInfo function, base.installelamcertificateinfo, sysinfoapi/InstallELAMCertificateInfo
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - InstallELAMCertificateInfo
 - sysinfoapi/InstallELAMCertificateInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
 - bcrypt.dll
api_name:
 - InstallELAMCertificateInfo
---

# InstallELAMCertificateInfo function


## -description

Installs the certificate information specified in the resource file, which is linked into the ELAM 
    driver at build time. This API is used by anti-malware vendors to launch the anti-malware software's user-mode 
    service as protected. For more information, see 
    <a href="/windows/desktop/Services/protecting-anti-malware-services-">Protecting Anti-Malware Services</a>.

## -parameters

### -param ELAMFile [in]

A handle to an ELAM driver file which contains the resource file with the certificate information. The handle 
       to the ELAM driver file must be opened for read access only and must not be shared for write access.

## -returns

If the function succeeds, the return value is TRUE.

If the function fails, the return value is FALSE. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Anti-malware vendors can use this API to register their anti-malware user-mode service that needs to be 
    launched as protected.  Note that the file handle supplied in the <i>hElamFile</i> parameter must be opened for read access 
    only and must not be shareable for write access.

For more information, see 
    <a href="/windows/desktop/Services/protecting-anti-malware-services-">Protecting Anti-Malware Services</a>.


#### Examples

Code example:


```cpp
HANDLE FileHandle = NULL;

FileHandle = CreateFile(<Insert Elam driver file name>,
                        FILE_READ_DATA,
                        FILE_SHARE_READ,
                        NULL,
                        OPEN_EXISTING,
                        FILE_ATTRIBUTE_NORMAL,
                        NULL
                        );

if (InstallElamCertificateInfo(FileHandle) == FALSE)
{
    Result = GetLastError();
    goto exitFunc;
}
```