---
UID: NF:faxdev.FaxDevAbortOperation
title: FaxDevAbortOperation function (faxdev.h)
description: The fax service calls the FaxDevAbortOperation function to request that the fax service provider (FSP) terminate the active fax operation for the fax job specified by the FaxHandle parameter. Each FSP must export the FaxDevAbortOperation function.
helpviewer_keywords: ["FaxDevAbortOperation","FaxDevAbortOperation function [Fax Service]","_mfax_faxdevabortoperation","fax._mfax_faxdevabortoperation","faxdev/FaxDevAbortOperation"]
old-location: fax\_mfax_faxdevabortoperation.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_3y26.htm
ms.date: 12/05/2018
ms.keywords: FaxDevAbortOperation, FaxDevAbortOperation function [Fax Service], _mfax_faxdevabortoperation, fax._mfax_faxdevabortoperation, faxdev/FaxDevAbortOperation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxDevAbortOperation
 - faxdev/FaxDevAbortOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxDev.h
api_name:
 - FaxDevAbortOperation
---

# FaxDevAbortOperation function


## -description

The fax service calls the <b>FaxDevAbortOperation</b> function to request that the fax service provider (FSP) terminate the active fax operation for the fax job specified by the <i>FaxHandle</i> parameter. Each FSP must export the <b>FaxDevAbortOperation</b> function.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a> function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>FaxDevAbortOperation</b> function is called asynchronously on an execution thread that is independent of the fax operation. It is usually necessary to synchronize access by multiple threads. For more information, see <a href="/windows/desktop/ProcThread/synchronizing-execution-of-multiple-threads">Synchronizing Execution of Multiple Threads</a>.

<b>FaxDevAbortOperation</b> should return after posting the abort request, rather than wait for the fax operation to end before returning.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-functions">Fax Service Provider Functions</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevendjob">FaxDevEndJob</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevstartjob">FaxDevStartJob</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>