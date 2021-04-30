---
UID: NF:faxdev.FaxDevStartJob
title: FaxDevStartJob function (faxdev.h)
description: The fax service calls the FaxDevStartJob function to initialize a new fax job. The fax service also calls FaxDevStartJob to signal the beginning of each fax operation to the fax service provider (FSP). Each FSP must export the FaxDevStartJob function.
helpviewer_keywords: ["FaxDevStartJob","FaxDevStartJob function [Fax Service]","_mfax_faxdevstartjob","fax._mfax_faxdevstartjob","faxdev/FaxDevStartJob"]
old-location: fax\_mfax_faxdevstartjob.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_5ode.htm
ms.date: 12/05/2018
ms.keywords: FaxDevStartJob, FaxDevStartJob function [Fax Service], _mfax_faxdevstartjob, fax._mfax_faxdevstartjob, faxdev/FaxDevStartJob
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
 - FaxDevStartJob
 - faxdev/FaxDevStartJob
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
 - FaxDevStartJob
---

# FaxDevStartJob function


## -description

The fax service calls the <b>FaxDevStartJob</b> function to initialize a new fax job. The fax service also calls <b>FaxDevStartJob</b> to signal the beginning of each fax operation to the fax service provider (FSP). Each FSP must export the <b>FaxDevStartJob</b> function.

## -parameters

### -param LineHandle [in]

Type: <b>HLINE</b>

Specifies a handle to the open line device associated with the fax job.

### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies the TAPI line device identifier associated with the fax job.

### -param FaxHandle [out]

Type: <b>PHANDLE</b>

Pointer to a variable that receives a fax handle associated with the fax job. The FSP must set this handle to a meaningful value; this handle usually specifies a pointer to a block of memory with job-specific instance data.

### -param CompletionPortHandle [in]

Type: <b>HANDLE</b>

Specifies a handle to an I/O completion port. For more information, see <a href="/windows/desktop/FileIO/i-o-completion-ports">I/O Completion Ports</a>.

### -param CompletionKey [in]

Type: <b>ULONG_PTR</b>

Specifies a completion key value. The fax service provider should pass this opaque value to the <a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a> function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>FaxDevStartJob</b> function provides an opportunity for the fax service provider to perform call setup.

The fax service calls <b>FaxDevStartJob</b> at the beginning of a new fax job and once for each fax operation. This is because each operation executes in a separate thread. It calls <b>FaxDevStartJob</b> just before the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a> function call for a fax send operation, and just before the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a> function call for a fax receive operation. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-operating-in-a-multithreaded-environment">Operating in a Multithreaded Environment</a>.

The FSP should create an I/O completion packet and call the <a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a> function when the FSP changes its status. One example of a status change is when the FSP finishes receiving or sending fax transmission pages. The completion packet must be a <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a> structure. The FSP must allocate memory for the structure from the heap indicated by the <i>HeapHandle</i> parameter passed to the <a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevinitialize">FaxDevInitialize</a> function. The fax service provider must pass the size of the memory allocated to the <i>dwNumberOfBytesTransferred</i> parameter of the PostQueuedCompletionStatus method. The fax service frees any memory allocated for the completion packet structure.

The FSP should use the <i>CompletionPortHandle</i> and <i>CompletionKey</i> parameters to post completion packets for FSP status changes. This method of status notification optimizes performance because the fax service does not need to poll FSPs to obtain updated status information. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-creating-a-completion-packet">Creating a Completion Packet</a>.

## -see-also

<a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-provider-functions">Fax Service Provider Functions</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevendjob">FaxDevEndJob</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevinitialize">FaxDevInitialize</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevreceive">FaxDevReceive</a>



<a href="/previous-versions/windows/desktop/api/faxdev/nf-faxdev-faxdevsend">FaxDevSend</a>



<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-using-the-fax-service-provider-api">Using the Fax Service Provider API</a>