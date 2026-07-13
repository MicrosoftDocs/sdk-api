---
UID: NF:setupapi.SetupGetInfPublishedNameW
title: SetupGetInfPublishedNameW function (setupapi.h)
description: The SetupGetInfPublishedName function retrieves the fully qualified file name (directory path and file name) of an INF file in the system INF file directory that corresponds to a specified INF file in the driver store or a specified INF file in the system INF file directory. (Unicode)
helpviewer_keywords: ["SetupGetInfPublishedName", "SetupGetInfPublishedName function [Device and Driver Installation]", "SetupGetInfPublishedNameW", "devinst.setupgetinfpublishedname", "setup-ref_c380d9fc-bc1c-4302-ba2b-b0bb7fde8d87.xml", "setupapi/SetupGetInfPublishedName"]
old-location: devinst\setupgetinfpublishedname.htm
tech.root: devinst
ms.assetid: 0379f8f4-9761-4216-b4d5-5752b6dc33a5
ms.date: 12/05/2018
ms.keywords: SetupGetInfPublishedName, SetupGetInfPublishedName function [Device and Driver Installation], SetupGetInfPublishedNameA, SetupGetInfPublishedNameW, devinst.setupgetinfpublishedname, setup-ref_c380d9fc-bc1c-4302-ba2b-b0bb7fde8d87.xml, setupapi/SetupGetInfPublishedName
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupGetInfPublishedNameW
 - setupapi/SetupGetInfPublishedNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupGetInfPublishedName
 - SetupGetInfPublishedNameW
---

# SetupGetInfPublishedNameW function


## -description

The <b>SetupGetInfPublishedName</b> function retrieves the fully qualified file name (directory path and file name) of an <a href="/windows-hardware/drivers/install/overview-of-inf-files">INF file</a> in the system INF file directory that corresponds to a specified INF file in the driver store or a specified INF file in the system INF file directory.

## -parameters

### -param DriverStoreLocation [in]

A pointer to a NULL-terminated string that contains the fully qualified file name (directory path and file name) of an INF file in the driver store. Alternatively, this parameter is a pointer to a NULL-terminated string that contains the name, and optionally the full directory path, of an INF file in the system INF file directory. For more information about how to specify the INF file, see the following <b>Remarks</b> section.

### -param ReturnBuffer [out]

A pointer to the buffer in which <b>SetupGetInfPublishedName</b> returns a NULL-terminated string that contains the fully qualified file name of the specified INF file in the system INF directory. The maximum path size is MAX_PATH. This pointer can be set to <b>NULL</b>. For information about how to determine the required size of the return buffer, see the following <b>Remarks</b> section.

### -param ReturnBufferSize [in]

The size, in characters, of the buffer supplied by <i>ReturnBuffer</i>.

### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the size, in characters, of the <i>ReturnBuffer</i> buffer. This parameter is optional and can be set to <b>NULL</b>.

## -returns

If <b>SetupGetInfPublishedName</b> succeeds, the function returns <b>TRUE</b>; otherwise, the function returns <b>FALSE</b>. To obtain extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the size, in characters, of the fully qualified file name of the requested INF file, including a null-terminator, is greater than <i>ReturnBufferSize</i>, the function will fail, and a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER.

## -remarks

To determine the size of the return buffer that is required to contain the fully qualified file name of the specified INF file in the system INF directory, call <b>SetupGetInfPublishedName</b> and set <i>ReturnBuffer</i> to <b>NULL</b>, <i>ReturnBufferSize</i> to zero, and supply <i>RequiredSize</i>. <b>SetupGetInfPublishedName</b> will return the required buffer size in <i>RequiredSize</i>.

When device installation preinstalls a <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> in the driver store, it creates two copies of the driver package INF file. Device installation adds one copy to the system INF directory and assigns that copy of the INF file a unique <i>published file name</i> of the form <i>OEMnnn.inf</i>. Device installation adds a second copy of the INF file to the driver store and assigns that copy the original INF file name.

<b>SetupGetInfPublishedName</b> returns the fully qualified file name of the INF file in the system INF file directory that matches the INF file, if any, that is supplied by <i>DriverStoreLocation</i>. <i>DriverStoreLocation </i> must specify the fully qualified file name of an INF file in the driver store or must specify the file name, and optionally the directory path, of an INF file in the system INF directory. For example, assume that the INF file for a driver package is <i>myinf.inf</i>, and that for this driver package, device installation installs the INF file <i>OEM1.inf</i> in the system INF directory C:<i>\Windows\inf</i>. Further assume that device installation installs the corresponding INF file copy C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf</i> in the driver store. In this case, the function returns C:<i>\Windows\inf\OEM1.inf</i> if <i>DriverStoreLocation</i> supplies one of the following strings: C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf, OEM1.inf</i>, or C:<i>\Windows\inf\OEM1.inf.</i>

Call the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfdriverstorelocationa">SetupGetInfDriverStoreLocation</a> function to retrieve the fully qualified file name of an INF file in the driver store that corresponds to a specified INF file in the system INF file directory or a specified file in the driver store.





> [!NOTE]
> The setupapi.h header defines SetupGetInfPublishedName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfdriverstorelocationa">SetupGetInfDriverStoreLocation</a>
