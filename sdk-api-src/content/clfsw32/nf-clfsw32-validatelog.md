---
UID: NF:clfsw32.ValidateLog
title: ValidateLog function (clfsw32.h)
author: windows-sdk-content
description: Validates the consistency of the log metadata and data before log archive and after log restore.
old-location: fs\validatelogrestore.htm
tech.root: Clfs
ms.assetid: dee4224e-bc94-42aa-95b9-226f13fd51ae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ValidateLog, ValidateLog function [Files], clfsw32/ValidateLog, fs.validatelogrestore
ms.topic: function
f1_keywords:
- clfsw32/ValidateLog
req.header: clfsw32.h
req.include-header: 
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
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Clfsw32.dll
api_name:
- ValidateLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ValidateLog function


## -description


Validates the consistency of   the log metadata and data before log archive and after log restore.


## -parameters




### -param pszLogFileName [in]

The name of the log. 

The  name is specified when creating the log  by using  <a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>. The following example identifies the format  to use:

<i>Log</i><b>:&lt;</b><i>LogName</i><b>&gt;[::&lt;</b><i>LogStreamName</i><b>&gt;]</b>

<b>&lt;</b><i>LogName</i><b>&gt;</b> corresponds to a valid file path  in  the   file system.

<b>&lt;</b><i>LogStreamName</i><b>&gt;</b> is  the unique name of a log stream in the dedicated log.   

For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/clfs/log-types">Log Types</a>.


### -param psaLogFile [in, optional]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a> structure that  specifies the security attributes of a log. 

This parameter can be <b>NULL</b>.


### -param pinfoBuffer [out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_information">CLFS_INFORMATION</a> structure that receives log metadata. 


### -param pcbBuffer [in, out]

A pointer to a variable that, on input, specifies the size of the <i>pinfoBuffer</i> metadata buffer, in bytes.  

On output, it receives the amount of information that is copied to the buffer, in bytes.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

The following list identifies the  possible error codes:




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_information">CLFS_INFORMATION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)">SECURITY_ATTRIBUTES</a>
 

 

