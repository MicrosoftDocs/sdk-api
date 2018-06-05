---
UID: NS:winbase._FILE_STANDARD_INFO
title: "_FILE_STANDARD_INFO"
author: windows-sdk-content
description: Receives extended information for the file.
old-location: fs\file_standard_info.htm
old-project: FileIO
ms.assetid: da3187de-7de2-4307-a083-ae5fff6d8096
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PFILE_STANDARD_INFO, FILE_STANDARD_INFO, FILE_STANDARD_INFO structure [Files], PFILE_STANDARD_INFO, PFILE_STANDARD_INFO structure pointer [Files], _FILE_STANDARD_INFO, fileextd/FILE_STANDARD_INFO, fileextd/PFILE_STANDARD_INFO, fs.file_standard_info, winbase/FILE_STANDARD_INFO, winbase/PFILE_STANDARD_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: FILE_STANDARD_INFO, *PFILE_STANDARD_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinBase.h
-	FileExtd.h
api_name:
-	FILE_STANDARD_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_STANDARD_INFO structure


## -description


Receives  extended information for the file. Used for file handles. Use only when calling 
   <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>.


## -struct-fields




### -field AllocationSize

The amount of space that is allocated for the file.


### -field EndOfFile

The end of the file.


### -field NumberOfLinks

The number of links to the file.


### -field DeletePending

<b>TRUE</b> if the file in the delete queue; otherwise, 
      <b>false</b>.


### -field Directory

<b>TRUE</b> if  the  file is a directory; otherwise, 
      <b>false</b>.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

