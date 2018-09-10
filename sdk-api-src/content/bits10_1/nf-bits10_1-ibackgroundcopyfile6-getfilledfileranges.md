---
UID: NF:bits10_1.IBackgroundCopyFile6.GetFilledFileRanges
title: IBackgroundCopyFile6::GetFilledFileRanges
author: windows-sdk-content
description: Returns the set of file ranges that have been downloaded.
old-location: bits\ibackgroundcopyfile6_getfilledfileranges.htm
tech.root: bits
ms.assetid: D3549C42-6642-4C3C-9D97-6F2F9732C48E
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetFilledFileRanges, GetFilledFileRanges method [BITS], GetFilledFileRanges method [BITS],IBackgroundCopyFile6 interface, IBackgroundCopyFile6 interface [BITS],GetFilledFileRanges method, IBackgroundCopyFile6.GetFilledFileRanges, IBackgroundCopyFile6::GetFilledFileRanges, bits.ibackgroundcopyfile6_getfilledfileranges, bits10_1/IBackgroundCopyFile6::GetFilledFileRanges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits10_1.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits10_1.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyFile6.GetFilledFileRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile6::GetFilledFileRanges


## -description


Returns the set of file ranges that have been downloaded.


## -parameters




### -param rangeCount

TBD


### -param ranges

TBD




#### - RangeCount [out]

The number of elements in <i>Ranges</i>.


#### - Ranges [out]

Array of <b>BG_FILE_RANGE</b> structures that describes the ranges that have been downloaded. Ranges will be merged together as much as possible. The ranges are ordered by offset.  When done, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free <i>Ranges</i>. 


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.  The error will be <b>E_OUTOFMEMORY</b> if the <i>Ranges</i> array could not be allocated and <b>BG_E_RANDOM_ACCESS_NOT_SUPPORTED</b> if the job is not a download job or if the server loses its ability to support download ranges.  




## -remarks



<b>GetFilledFileRanges</b> can be requested for any download job that also meets the requirements for <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> jobs.  


The requirements for a <b>BITS_JOB_PROPERTY_ON_DEMAND_MODE</b> job is that the transfer must be a <b>DOWNLOAD</b> job.  The job must not be <b>DYNAMIC</b> and the server must be an HTTP or HTTPS server and the server requirements for range support must all be met.
For more information, see <a href="https://msdn.microsoft.com/35af422b-62e4-41fd-8890-579ccf016c83">HTTP Requirements for BITS Downloads</a>.




## -see-also




<a href="https://msdn.microsoft.com/FE3B1BAB-2634-4BE0-91B7-F97041CB3655">IBackgroundCopyFile6</a>
 

 

