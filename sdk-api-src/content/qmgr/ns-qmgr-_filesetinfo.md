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

# _FILESETINFO structure


## -description


<p class="CCE_Message">[Queue Manager (QMGR) is available for use in the operating systems specified in the Requirements section.  It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/ce91f87c-8273-4a1c-99e0-ef55e2a50334">Background Intelligent Transfer Service (BITS)</a>.]

The <b>FILESETINFO</b> structure identifies the remote and local names of the file to download.


## -struct-fields




### -field bstrRemoteFile

Null-terminated string that contains the name of the file on the server (for example, <b>http://</b><i>ServerName</i><b>/</b><i>Path</i><b>/</b><i>FileName</i><b>.</b><i>ext</i>). The format of the name must conform to the transfer protocol you use. You cannot use wildcards in the path or file name. The URL must only contain legal URL characters; no escape processing is performed. The URL is limited to 2,200 characters, not including the terminating null character. 



					


### -field bstrLocalFile

Null-terminated string that contains the name of the file on the client. The file name must include the full path, for example, <b>D:\</b><i>MyApp</i><b>\</b><i>UpdatesPath</i><b>\</b><i>FileName</i><b>.</b><i>ext</i>. You cannot use wildcards in the path or file name, and directories in the path must exist. The path is limited to MAX_PATH, not including the terminating null character. The user must have permission to write to the local directory for downloads and uploads that request a reply. BITS does not support NTFS streams. Instead of using network drives, which are session specific, use UNC paths (for example, <b>\\</b><i>ServerName</i><b>\</b><i>ShareName</i><b>\</b><i>Path</i><b>\</b><i>FileName</i><b>.</b><i>ext</i>).


### -field dwSizeHint

Not supported.

