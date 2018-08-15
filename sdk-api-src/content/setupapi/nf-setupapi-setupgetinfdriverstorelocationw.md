---
UID: NF:setupapi.SetupGetInfDriverStoreLocationW
title: SetupGetInfDriverStoreLocationW function
author: windows-sdk-content
description: The SetupGetInfDriverStoreLocation function retrieves the fully qualified file name (directory path and file name) of an INF file in the driver store that corresponds to a specified INF file in the system INF file directory or a specified INF file in the driver store.
old-location: devinst\setupgetinfdriverstorelocation.htm
old-project: devinst
ms.assetid: 34131e9e-2e0e-4098-a988-3dadbf1789af
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupGetInfDriverStoreLocation, SetupGetInfDriverStoreLocation function [Device and Driver Installation], SetupGetInfDriverStoreLocationA, SetupGetInfDriverStoreLocationW, devinst.setupgetinfdriverstorelocation, setup-ref_349dd5f9-d925-4bdf-b99d-b8abef1eb12b.xml, setupapi/SetupGetInfDriverStoreLocation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupGetInfDriverStoreLocation
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupGetInfDriverStoreLocationW function


## -description


The <b>SetupGetInfDriverStoreLocation</b> function retrieves the fully qualified file name (directory path and file name) of an <a href="https://msdn.microsoft.com/library/Ff549520(v=VS.85).aspx">INF file</a> in the driver store that corresponds to a specified INF file in the system INF file directory or a specified INF file in the driver store.


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



If <b>SetupGetInfDriverStoreLocation</b> succeeds, the function returns <b>TRUE</b>; otherwise, the function returns <b>FALSE</b>. To obtain extended error information, call <a href="http://go.microsoft.com/fwlink/p/?linkid=74036">GetLastError</a>. 

If the size, in characters, of the fully qualified file name of the requested INF file, including a null-terminator, is greater than <i>ReturnBufferSize</i>, the function will fail, and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=74036">GetLastError</a> will return ERROR_INSUFFICIENT_BUFFER. 




## -remarks



To determine the size of the return buffer that is required to contain the fully qualified file name of the specified INF file in the driver store, call <b>SetupGetInfDriverStoreLocation</b> and set <i>ReturnBuffer</i> to <b>NULL</b>, <i>ReturnBufferSize</i> to zero, and supply <i>RequiredSize</i>. <b>SetupGetInfDriverStoreLocation</b> will return the required buffer size in <i>RequiredSize</i>.

When device installation preinstalls a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> in the driver store, it creates two copies of the driver package INF file. Device installation installs one copy in the system INF directory and assigns that copy of the INF file a unique <i>published file name</i> of the form <i>OEMnnn.inf</i>. Device installation installs a second copy of the INF file in the driver store and assigns that copy the original INF file name.

<b>SetupGetInfDriverStoreLocation</b> returns the fully qualified file name of the INF file in the driver store that matches the INF file, if any, that is supplied by <i>FileName</i>. <i>Filename</i> must specify the file name, and optionally the directory path, of an INF file in the system INF directory. Alternatively, <i>Filename</i> must specify the fully qualified file name of an INF file in the driver store. 

For example, assume that the INF file for a driver package is <i>Myinf.inf</i>, and that for this driver package, device installation installs the INF file <i>OEM1.inf</i> in the system INF directory C:<i>\Windows\inf.</i> Further assume that device installation installs the corresponding INF file copy C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf</i> in the driver store. In this case, the function returns C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf</i> if <i>FileName</i> supplies one of the following strings: <i>OEM1.inf</i>, C:<i>\Windows\inf\OEM1.inf</i>, or C:<i>\windows\system32\driverstore\filerepository\myinf_12345678\myinf.inf.</i>

<a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">Class installers</a> and <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">co-installers</a> can use <b>SetupGetInfDriverStoreLocation</b> to access files in a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> that is preinstalled in the driver store. To determine the path of the driver package in the driver store, the installer does the following:

<ol>
<li>
Call <a href="https://msdn.microsoft.com/42f3668c-8112-4cc0-bce8-b0b3886c45fb">SetupDiGetDriverInfoDetail</a> to retrieve a <a href="https://msdn.microsoft.com/6e16a90a-a876-471c-917b-a26229a9187a">SP_DRVINFO_DETAIL_DATA</a> structure for a driver. The <b>InfFileName</b> member of this structure contains the fully qualified file name of the driver INF file in the system INF directory.

</li>
<li>
Call <b>SetupGetInfDriverStoreLocation</b> and supply the fully qualified file name of the driver INF file that was retrieved by calling <b>SetupDiGetDriverInfoDetail</b>. <b>SetupGetInfDriverStoreLocation</b> will return the fully qualified file name of the driver INF file in the driver store. The directory path part of the fully qualified file name of the INF file is the path of the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> files. 

</li>
</ol>
<div class="alert"><b>Note</b>  <b>SetupGetInfDriverStoreLocation</b> does not process the contents of the INF file that is specified in <i>FileName</i>. You cannot use this function to perform a content-specific search for an INF file in the driver store.</div>
<div> </div>
Call the <a href="https://msdn.microsoft.com/0379f8f4-9761-4216-b4d5-5752b6dc33a5">SetupGetInfPublishedName</a> function to retrieve the fully qualified file name of an <a href="https://msdn.microsoft.com/library/Ff549520(v=VS.85).aspx">INF file</a> in the system INF file directory that corresponds to a specified INF file in the system INF file directory or a specified file in the driver store.




## -see-also




<a href="https://msdn.microsoft.com/d9aba6c9-1b23-4ce0-b796-904b39bec3ac">SP_ALTPLATFORM_INFO</a>



<a href="https://msdn.microsoft.com/6e16a90a-a876-471c-917b-a26229a9187a">SP_DRVINFO_DETAIL_DATA</a>



<a href="https://msdn.microsoft.com/42f3668c-8112-4cc0-bce8-b0b3886c45fb">SetupDiGetDriverInfoDetail</a>



<a href="https://msdn.microsoft.com/0379f8f4-9761-4216-b4d5-5752b6dc33a5">SetupGetInfPublishedName</a>
 

 

