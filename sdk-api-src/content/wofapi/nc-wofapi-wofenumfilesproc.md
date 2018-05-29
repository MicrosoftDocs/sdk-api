---
UID: NC:wofapi.WofEnumFilesProc
title: WofEnumFilesProc
author: windows-sdk-content
description: Callback function that gets called for each file backed by an external data source, such as a WIM file.
old-location: fs\wofenumfilesproc.htm
old-project: FileIO
ms.assetid: E710869D-68A9-4E30-96DE-6313A5A182D8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WofEnumFilesProc, WofEnumFilesProc function, WofEnumFilesProc function pointer [Files], fs.wofenumfilesproc, wofapi/WofEnumFilesProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wofapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: WNV_REDIRECT_PARAM, *PWNV_REDIRECT_PARAM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	wofapi.h
api_name:
-	WofEnumFilesProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WofEnumFilesProc callback function


## -description


Callback function that gets called for each file backed by an external data source, such as a WIM file.


## -parameters




### -param FilePath [in]

Specifies the path to the file which is backed by an external data source.


### -param ExternalFileInfo [in]

Points to a buffer containing information about the data source backing the file.  The type of this buffer depends on the provider; data structures for each provider are:

<table>
<tr>
<td>WOF_PROVIDER_WIM</td>
<td>WIM_EXTERNAL_FILE_INFO</td>
</tr>
<tr>
<td>WOF_PROVIDER_FILE</td>
<td>WOF_FILE_COMPRESSION_INFO</td>
</tr>
</table>
 


### -param UserData [in, optional]

Optional user defined data.


## -returns



A boolean value that indicates whether the enumeration was successful. The enumeration will stop if this callback function returns FALSE.



