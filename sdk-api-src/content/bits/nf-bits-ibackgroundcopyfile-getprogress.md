---
UID: NF:bits.IBackgroundCopyFile.GetProgress
title: IBackgroundCopyFile::GetProgress
author: windows-sdk-content
description: Retrieves information on the progress of the file transfer.
old-location: bits\ibackgroundcopyfile_getprogress.htm
tech.root: Bits
ms.assetid: e72ec5af-7c21-48f8-b027-76a6c9e67f5e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetProgress, GetProgress method [BITS], GetProgress method [BITS],IBackgroundCopyFile interface, IBackgroundCopyFile interface [BITS],GetProgress method, IBackgroundCopyFile.GetProgress, IBackgroundCopyFile::GetProgress, _drz_ibackgroundcopyfile_getprogress, bits.ibackgroundcopyfile_getprogress, bits/IBackgroundCopyFile::GetProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyFile.GetProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBackgroundCopyFile::GetProgress


## -description


Retrieves information on the progress of the file transfer.


## -parameters




### -param pVal

TBD




#### - pProgress [out]

Structure whose members indicate the progress of the file transfer. For details on the type of progress information available, see the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362801(v=VS.85).aspx">BG_FILE_PROGRESS</a> structure. 


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362801(v=VS.85).aspx">BG_FILE_PROGRESS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362881(v=VS.85).aspx">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363034(v=VS.85).aspx">IBackgroundCopyJob::GetProgress</a>
 

 

