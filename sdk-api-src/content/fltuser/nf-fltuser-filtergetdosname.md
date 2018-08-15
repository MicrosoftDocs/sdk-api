---
UID: NF:fltuser.FilterGetDosName
title: FilterGetDosName function
author: windows-sdk-content
description: The FilterGetDosName function returns the MS-DOS device name that corresponds to the given volume name.
old-location: ifsk\filtergetdosname.htm
old-project: ifsk
ms.assetid: f7c14e1f-c57f-4780-9936-3a47a4c0ca12
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FilterGetDosName, FilterGetDosName function [Installable File System Drivers], FltWin32ApiRef_46945955-c739-4b9c-bbf8-54c451c26716.xml, fltuser/FilterGetDosName, ifsk.filtergetdosname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fltuser.h
req.include-header: Fltuser.h
req.redist: 
req.target-type: Universal
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterGetDosName
product: Windows
targetos: Windows
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
req.product: Internet Explorer 5
---

# FilterGetDosName function


## -description


The <b>FilterGetDosName</b> function returns the MS-DOS device name that corresponds to the given volume name. 


## -parameters




### -param lpVolumeName [in]

Pointer to a NULL-terminated wide-character string containing the volume name. 

The <i>lpVolumeName</i> input string can be any of the following. The trailing backslash (\) is optional. 

<ul>
<li>
A drive letter, such as "D:\"

</li>
<li>
A path to a volume mount point, such as "c:\mnt\edrive\"

</li>
<li>
A unique volume identifier (also called a <i>volume GUID name</i>), such as "\??\Volume{7603f260-142a-11d4-ac67-806d6172696f}\"

</li>
<li>
A nonpersistent device name (also called a <i>target name</i> or an <i>NT device name</i>), such as "\Device\HarddiskVolume1\"

</li>
</ul>
This parameter is required and cannot be <b>NULL</b>. 


### -param lpDosName [out]

Pointer to a caller-allocated buffer that receives the MS-DOS device name as a NULL-terminated wide-character string. 


### -param dwDosNameBufferSize [in]

Size, in wide characters, of the buffer that <i>lpDosName </i>points to. 


## -returns



<b>FilterGetDosName</b> returns S_OK if successful. Otherwise, it returns an error value. 




## -remarks



<b>FilterGetDosName</b> returns the volume's drive letter if it has one. If no drive letter is assigned to the volume, <b>FilterGetDosName</b> returns a path to a volume mount point (also called a <i>mount point name</i>). If no drive letters or mount points are defined for the volume, <b>FilterGetDosName</b> returns S_OK, and <i>lpDosName</i> receives <b>NULL</b>. 




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=139080">DefineDosDevice</a>



<a href="https://msdn.microsoft.com/50815b33-d417-4499-9423-f65697396200">FltGetVolumeName</a>



<a href="https://msdn.microsoft.com/8574e5cf-5bbf-4606-931f-e27b2aa7b7fa">IoQueryFileDosDeviceName</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=139081">QueryDosDevice</a>
 

 

