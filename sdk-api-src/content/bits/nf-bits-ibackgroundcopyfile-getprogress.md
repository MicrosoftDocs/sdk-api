---
UID: NF:bits.IBackgroundCopyFile.GetProgress
title: IBackgroundCopyFile::GetProgress method
author: windows-driver-content
description: Retrieves information on the progress of the file transfer.
old-location: bits\ibackgroundcopyfile_getprogress.htm
old-project: Bits
ms.assetid: e72ec5af-7c21-48f8-b027-76a6c9e67f5e
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: GetProgress method [BITS], GetProgress method [BITS], IBackgroundCopyFile interface, GetProgress,IBackgroundCopyFile.GetProgress, IBackgroundCopyFile, IBackgroundCopyFile interface [BITS], GetProgress method, IBackgroundCopyFile::GetProgress, _drz_ibackgroundcopyfile_getprogress, bits.ibackgroundcopyfile_getprogress, bits/IBackgroundCopyFile::GetProgress
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyFile.GetProgress
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyFile::GetProgress method


## -description


Retrieves information on the progress of the file transfer.


## -parameters




### -param pVal






#### - pProgress [out]

Structure whose members indicate the progress of the file transfer. For details on the type of progress information available, see the 
<a href="https://msdn.microsoft.com/322363b4-081e-4100-9087-e34c21a3ffae">BG_FILE_PROGRESS</a> structure. 


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/322363b4-081e-4100-9087-e34c21a3ffae">BG_FILE_PROGRESS</a>



<a href="https://msdn.microsoft.com/fae9cf56-c211-445b-b962-9a9d7d67c59c">IBackgroundCopyFile</a>



<a href="https://msdn.microsoft.com/30aae990-1cc1-468b-9e5f-7ef5ce6eeb9a">IBackgroundCopyJob::GetProgress</a>
 

 

