---
UID: NF:faxdev.FaxDevAbortOperation
title: FaxDevAbortOperation function
author: windows-sdk-content
description: The fax service calls the FaxDevAbortOperation function to request that the fax service provider (FSP) terminate the active fax operation for the fax job specified by the FaxHandle parameter. Each FSP must export the FaxDevAbortOperation function.
old-location: fax\_mfax_faxdevabortoperation.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_3y26.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FaxDevAbortOperation, FaxDevAbortOperation function [Fax Service], _mfax_faxdevabortoperation, fax._mfax_faxdevabortoperation, faxdev/FaxDevAbortOperation
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
 - FaxDevAbortOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxDevAbortOperation function


## -description


The fax service calls the <b>FaxDevAbortOperation</b> function to request that the fax service provider (FSP) terminate the active fax operation for the fax job specified by the <i>FaxHandle</i> parameter. Each FSP must export the <b>FaxDevAbortOperation</b> function.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a> function.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>FaxDevAbortOperation</b> function is called asynchronously on an execution thread that is independent of the fax operation. It is usually necessary to synchronize access by multiple threads. For more information, see <a href="https://msdn.microsoft.com/74af0502-dae1-438c-8e4b-7663093b3fe3">Synchronizing Execution of Multiple Threads</a>.

<b>FaxDevAbortOperation</b> should return after posting the abort request, rather than wait for the fax operation to end before returning.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684546(v=VS.85).aspx">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684550(v=VS.85).aspx">FaxDevEndJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684541(v=VS.85).aspx">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693428(v=VS.85).aspx">Using the Fax Service Provider API</a>
 

 

