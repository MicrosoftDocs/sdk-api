---
UID: NF:clfsw32.SetLogArchiveTail
title: SetLogArchiveTail function
author: windows-sdk-content
description: Sets the last archived log sequence number (LSN) or archive tail of an archivable log.
old-location: fs\setlogarchivetail.htm
old-project: Clfs
ms.assetid: 0cdd0b85-d53e-432d-962d-9e89143ec4c7
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetLogArchiveTail, SetLogArchiveTail function [Files], clfsw32/SetLogArchiveTail, fs.setlogarchivetail
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - SetLogArchiveTail
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# SetLogArchiveTail function


## -description


Sets the last archived log sequence number (LSN) or <i>archive tail</i> of an archivable log.


## -parameters




### -param hLog [in]

A handle to the log that is obtained from <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>.  

The log handle can refer to a dedicated or multiplexed log.


### -param plsnArchiveTail [in]

A pointer to a <a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a> structure that specifies a valid physical LSN in the log.


<div class="alert"><b>Note</b>  For handles to both a physical log or a log stream, <i>plsnArchiveTail</i> is a physical LSN, because it refers to a record address in the physical log.</div>
<div> </div>



### -param OPTIONAL

TBD




#### - pReserved [in, out, optional]

This parameter is reserved and should be set to <b>NULL</b>. 


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

The following  list identifies the possible error codes:




## -remarks



If there are any archive contexts obtained from <a href="https://msdn.microsoft.com/dfdad56a-7485-4c23-852e-819980ecd5e9">PrepareLogArchive</a> that are not terminated with <a href="https://msdn.microsoft.com/885356e1-f7c4-4f3f-98c3-fb9b1d339e22">TerminateLogArchive</a>, the change does not take effect until all archives are complete. While there are outstanding archive contexts, only the greatest archive tail is applied.




## -see-also




<a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/e6571cb0-8453-4db0-9a33-17339c4ea223">RemoveLogContainer</a>



<a href="https://msdn.microsoft.com/adc35813-7368-4d8c-ad2b-1bb0824ad019">RemoveLogContainerSet</a>
 

 

