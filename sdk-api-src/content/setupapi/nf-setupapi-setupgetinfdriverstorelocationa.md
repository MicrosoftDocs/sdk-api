---
UID: NF:setupapi.SetupGetInfDriverStoreLocationA
title: SetupGetInfDriverStoreLocationA function (setupapi.h)
description: The SetupGetInfDriverStoreLocation function retrieves the fully qualified file name (directory path and file name) of an INF file in the driver store that corresponds to a specified INF file in the system INF file directory or a specified INF file in the driver store. (ANSI)
helpviewer_keywords: ["SetupGetInfDriverStoreLocationA", "setup-ref_349dd5f9-d925-4bdf-b99d-b8abef1eb12b.xml"]
old-location: devinst\setupgetinfdriverstorelocation.htm
tech.root: devinst
ms.assetid: 34131e9e-2e0e-4098-a988-3dadbf1789af
ms.date: 12/05/2018
ms.keywords: SetupGetInfDriverStoreLocation, SetupGetInfDriverStoreLocation function [Device and Driver Installation], SetupGetInfDriverStoreLocationA, SetupGetInfDriverStoreLocationW, devinst.setupgetinfdriverstorelocation, setup-ref_349dd5f9-d925-4bdf-b99d-b8abef1eb12b.xml, setupapi/SetupGetInfDriverStoreLocation
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
 - SetupGetInfDriverStoreLocationA
 - setupapi/SetupGetInfDriverStoreLocationA
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
 - SetupGetInfDriverStoreLocation - SetupGetInfDriverStoreLocationA
---

# SetupGetInfDriverStoreLocationA function


## -description

The <b>SetupGetInfDriverStoreLocation</b> function retrieves the fully qualified file name (directory path and file name) of an <a href="/windows-hardware/drivers/install/overview-of-inf-files">INF file</a> in the driver store that corresponds to a specified INF file in the system INF file directory or a specified INF file in the driver store.

## -parameters

### -param FileName [in]

A pointer to a NULL-terminated string that contains the name, and optionally the full directory path, of an INF file in the system INF file directory. Alternatively, this parameter is a pointer to a NULL-terminated string that contains the fully qualified file name (directory path and file name) of an INF file in the driver store. 

For more information about how to specify the INF file, see the following <b>Remarks</b> section.

### -param AlternatePlatformInfo [in, optional]

Reserved for system use.

### -param LocaleName [in, optional]

Reserved for system use.

### -param ReturnBuffer [out]

A pointer to a buffer in which the function returns a NULL-terminated string that contains the fully qualified file name of the specified INF file. This parameter can be set to <b>NULL</b>. The maximum supported path size is MAX_PATH. For information about how to determine the required size of the buffer, see the following <b>Remarks</b> section.

### -param ReturnBufferSize [in]

The size, in characters, of the buffer supplied by <i>ReturnBuffer</i>.

### -param RequiredSize [out, optional]

A pointer to a DWORD-typed variable that receives the size, in characters, of the <i>ReturnBuffer</i> buffer. This parameter is optional and can be set to <b>NULL</b>.

## -returns

If <b>SetupGetInfDriverStoreLocation</b> succeeds, the function returns <b>TRUE</b>; otherwise, the function returns <b>FALSE</b>. To obtain extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

If the size, in characters, of the fully qualified file name of the requested INF file, including a null-terminator, is greater than <i>ReturnBufferSize</i>, the function will fail, and a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER.

## -remarks

To determine the size of the return buffer that is required to contain the fully qualified file name of the specified INF file in the driver store, call <b>SetupGetInfDriverStoreLocation</b> and set <i>ReturnBuffer</i> to <b>NULL</b>, <i>ReturnBufferSize</i> to zero, and supply <i>RequiredSize</i>. <b>SetupGetInfDriverStoreLocation</b> will return the required buffer size in <i>RequiredSize</i>.

When device installation preinstalls a <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> in the driver store, it creates two copies of the driver package INF file. Device installation installs one copy in the system INF directory and assigns that copy of the INF file a unique <i>published file name</i> of the form <i>OEMnnn.inf</i>. Device installation installs a second copy of the INF file in the driver store and assigns that copy the original INF file name.

<b>SetupGetInfDriverStoreLocation</b> returns the fully qualified file name of the INF file in the driver store that matches the INF file, if any, that is supplied by <i>FileName</i>. <i>Filename</i> must specify the file name, and optionally the directory path, of an INF file in the system INF directory. Alternatively, <i>Filename</i> must specify the fully qualified file name of an INF file in the driver store. 

For example, assume that the INF file for a driver package is <i>Myinf.inf</i>, and that for this driver package, device installation installs the INF file <i>OEM1.inf</i> in the system INF directory C:<i>\Windows\inf.</i> Further assume that device installation installs the corresponding INF file copy C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf</i> in the driver store. In this case, the function returns C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf</i> if <i>FileName</i> supplies one of the following strings: <i>OEM1.inf</i>, C:<i>\Windows\inf\OEM1.inf</i>, or C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf.</i>

<a href="/windows-hardware/drivers/">Class installers</a> and <a href="/windows-hardware/drivers/">co-installers</a> can use <b>SetupGetInfDriverStoreLocation</b> to access files in a <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> that is preinstalled in the driver store. To determine the path of the driver package in the driver store, the installer does the following:

<ol>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinfodetaila">SetupDiGetDriverInfoDetail</a> to retrieve a <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_detail_data_a">SP_DRVINFO_DETAIL_DATA</a> structure for a driver. The <b>InfFileName</b> member of this structure contains the fully qualified file name of the driver INF file in the system INF directory.

</li>
<li>
Call <b>SetupGetInfDriverStoreLocation</b> and supply the fully qualified file name of the driver INF file that was retrieved by calling <b>SetupDiGetDriverInfoDetail</b>. <b>SetupGetInfDriverStoreLocation</b> will return the fully qualified file name of the driver INF file in the driver store. The directory path part of the fully qualified file name of the INF file is the path of the <a href="/windows-hardware/drivers/install/difx-guidelines">driver package</a> files. 

</li>
</ol>
<div class="alert"><b>Note</b>  <b>SetupGetInfDriverStoreLocation</b> does not process the contents of the INF file that is specified in <i>FileName</i>. You cannot use this function to perform a content-specific search for an INF file in the driver store.</div>
<div> </div>
Call the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfpublishednamea">SetupGetInfPublishedName</a> function to retrieve the fully qualified file name of an <a href="/windows-hardware/drivers/install/overview-of-inf-files">INF file</a> in the system INF file directory that corresponds to a specified INF file in the system INF file directory or a specified file in the driver store.





> [!NOTE]
> The setupapi.h header defines SetupGetInfDriverStoreLocation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/win32/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_detail_data_a">SP_DRVINFO_DETAIL_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinfodetaila">SetupDiGetDriverInfoDetail</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupgetinfpublishednamea">SetupGetInfPublishedName</a>
