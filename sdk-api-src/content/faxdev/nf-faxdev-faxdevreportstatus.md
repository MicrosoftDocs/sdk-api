---
UID: NF:faxdev.FaxDevReportStatus
title: FaxDevReportStatus function
author: windows-sdk-content
description: The fax service calls the FaxDevReportStatus function to query a fax service provider (FSP) for status information about an individual active fax operation, or for status information after a failed fax operation.
old-location: fax\_mfax_faxdevreportstatus.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxfspapiref_65gz.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: FaxDevReportStatus, FaxDevReportStatus function [Fax Service], _mfax_faxdevreportstatus, fax._mfax_faxdevreportstatus, faxdev/FaxDevReportStatus
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
 - FaxDevReportStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxDevReportStatus function


## -description


The fax service calls the <b>FaxDevReportStatus</b> function to query a fax service provider (FSP) for status information about an individual active fax operation, or for status information after a failed fax operation. Each FSP must export the <b>FaxDevReportStatus</b> function.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax handle returned by the <a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a> function that is associated with the fax job.


### -param FaxStatus [out]

Type: <b>PFAX_DEV_STATUS</b>

Pointer to a <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure that receives status and identification information. This parameter can also be a <b>NULL</b> pointer. For more information, see the following Remarks section.


### -param FaxStatusSize [in]

Type: <b>DWORD</b>

Specifies the size, in bytes, of the buffer pointed to by the <i>FaxStatus</i> parameter.


### -param FaxStatusSizeRequired [out]

Type: <b>LPDWORD</b>

Pointer to a variable that receives the calculated size, in bytes, of the buffer required to hold a <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure. For more information, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

<div class="alert"><b>Note</b>  For a successful send, FaxDevSend() should return <b>TRUE</b> and FaxDevReportStatus() should return FS_COMPLETED. For an unsuccessful send, FaxDevSend() should return <b>FALSE</b>, and FaxDevReportStatus() should return any of the following codes: FS_LINE_UNAVAILABLE, FS_NO_ANSWER, FS_NO_DIAL_TONE, FS_DISCONNECTED, FS_BUSY, FS_NOT_FAX_CALL, or FS_FATAL_ERROR. If after a failed fax the fax should not be re-sent, FaxDevReportStatus() should return any code other than those listed here.</div>
<div> </div>



## -remarks



To obtain status information for the operation, the <b>FaxDevReportStatus</b> function is called asynchronously on an execution thread that is independent of the fax operation. It is usually necessary to synchronize access by multiple threads. For more information, see <a href="https://msdn.microsoft.com/74af0502-dae1-438c-8e4b-7663093b3fe3">Synchronizing Execution of Multiple Threads</a>. 
            

If the <i>FaxStatusSize</i> parameter is equal to zero, and <i>FaxStatus</i> is a <b>NULL</b> pointer, the FSP must calculate the size, in bytes, of the buffer required to hold a <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure. The FSP must return this value in the <i>FaxStatusSizeRequired</i> parameter. The fax service will then allocate the required memory. It will also return both the memory size in the <i>FaxStatusSize</i> parameter, and a pointer to that memory in the <i>FaxStatus</i> parameter. 
            

The FSP must set all of the members of the <a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a> structure with status information for the active fax operation. The fax service allocates the memory for the strings pointed to by the <b>CSI</b>, <b>CallerId</b>, and <b>RoutingInfo</b> members. The size of the memory the service allocates is equal to <b>sizeof(FAX_DEV_STATUS) + FAXDEVREPORTSTATUS_SIZE</b>. The FSP must place the strings in the block of memory that immediately follows the <b>FAX_DEV_STATUS</b> structure. The <b>CSI</b>, <b>CallerId</b>, and <b>RoutingInfo</b> members must point to the location of the strings in the memory block.
            




## -see-also




<a href="https://msdn.microsoft.com/b5d024c2-36f9-4f70-abab-3824f3612089">FAX_DEV_STATUS</a>



<a href="https://msdn.microsoft.com/402583fd-aef8-4197-a41e-870825c58351">Fax Service Provider Functions</a>



<a href="https://msdn.microsoft.com/40f647ba-05ed-453a-8eea-729b2f59ac05">FaxDevStartJob</a>



<a href="https://msdn.microsoft.com/a8788e8a-e97c-4082-8e89-b6f4a7568d3a">Using the Fax Service Provider API</a>
 

 

