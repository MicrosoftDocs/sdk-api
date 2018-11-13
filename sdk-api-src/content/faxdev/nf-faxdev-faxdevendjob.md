---
UID: NF:faxdev.FaxDevEndJob
title: FaxDevEndJob function
author: windows-sdk-content
description: The fax service calls the FaxDevEndJob function after the last fax operation in a fax job. Each fax service provider (FSP) must export the FaxDevEndJob function.
old-location: fax\_mfax_faxdevendjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_9yua.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: FaxDevEndJob, FaxDevEndJob function [Fax Service], _mfax_faxdevendjob, fax._mfax_faxdevendjob, faxdev/FaxDevEndJob
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: faxdev.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevEndJob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxDevEndJob function


## -description


The fax service calls the <b>FaxDevEndJob</b> function after the last fax operation in a fax job. Each fax service provider (FSP) must export the <b>FaxDevEndJob</b> function.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The FSP should perform necessary cleanup tasks for the fax job when the fax service calls <b>FaxDevEndJob</b>. Cleanup should include deallocation of memory for any job-specific instance data that was allocated in the call to the <a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a> function. 

Note that if the fax service calls <b>FaxDevEndJob</b>, it will also call the <b>FaxDevEndJob</b> function, even if an operation has been terminated by the <a href="https://msdn.microsoft.com/en-us/library/ms684537(v=VS.85).aspx">FaxDevAbortOperation</a> function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684546(v=VS.85).aspx">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684537(v=VS.85).aspx">FaxDevAbortOperation</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693428(v=VS.85).aspx">Using the Fax Service Provider API</a>
 

 

