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

# SetupLogFileA function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupLogFile</b> function adds an entry to the log file.


## -parameters




### -param FileLogHandle [in]

Handle to the file log as returned by 
<a href="https://msdn.microsoft.com/fac7abac-76a9-456a-843a-e1048df268b7">SetupInitializeFileLog</a>. The caller must not have passed SPFILELOG_QUERYONLY when the log file was initialized.


### -param LogSectionName [in]

Optional pointer to the name for a logical grouping of names within the log file. You should use a <b>null</b>-terminated string.  Required if SPFILELOG_SYSTEMLOG was not passed when the file log was initialized. Otherwise, this parameter can be <b>NULL</b>.


### -param SourceFilename

TBD


### -param TargetFilename

TBD


### -param Checksum [in]

Optional pointer to a  checksum value. Required for the system log.


### -param DiskTagfile [in]

Optional pointer to the tagfile for the media from which the file was installed. You should use a <b>null</b>-terminated string. The <b>null</b>-terminated string should not exceed the size of the destination buffer. Ignored for the system log if SPFILELOG_OEMFILE is not specified. Required for the system log if SPFILELOG_OEMFILE is specified. Otherwise, this parameter can be <b>NULL</b>.


### -param DiskDescription [in]

Optional pointer to the human-readable description of the media from which the file was installed. You should use a <b>null</b>-terminated string.  Ignored for the system log if SPFILELOG_OEMFILE is not specified in the <i>Flags</i> parameter.  Required for the system log if SPFILELOG_OEMFILE is specified in the Flags parameter. Otherwise, this parameter can be <b>NULL</b>.



### -param OtherInfo [in]

Optional pointer to additional information to be associated with the file. You should use a <b>null</b>-terminated string.  This parameter can be <b>NULL</b>.



### -param Flags [in]

This parameter can be SPFILELOG_OEMFILE, which is meaningful only for the system log and indicates that the file is not supplied by Microsoft. This parameter can be used to convert an existing file's entry, such as when an OEM overwrites a Microsoft-supplied system file.


#### - SourceFileName [in]

Name of the file as it exists on the source media from which it was installed. This name should be in whatever format is meaningful to the caller. You should use a <b>null</b>-terminated string.


#### - TargetFileName [in]

Name of the file as it exists on the target. This name should be in whatever format is meaningful to the caller. You should use a <b>null</b>-terminated string.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/a26d2c24-7092-40b0-9ae9-e7edf68aeb3d">SetupRemoveFileLogEntry</a>
 

 

