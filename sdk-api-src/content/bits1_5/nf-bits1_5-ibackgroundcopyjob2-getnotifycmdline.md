---
UID: NF:bits1_5.IBackgroundCopyJob2.GetNotifyCmdLine
title: IBackgroundCopyJob2::GetNotifyCmdLine (bits1_5.h)
author: windows-sdk-content
description: Retrieves the program to execute when the job enters the error or transferred state.
old-location: bits\ibackgroundcopyjob2_getnotifycmdline.htm
tech.root: Bits
ms.assetid: 62978315-e893-4617-8e6d-63bab8204913
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNotifyCmdLine, GetNotifyCmdLine method [BITS], GetNotifyCmdLine method [BITS],IBackgroundCopyJob2 interface, IBackgroundCopyJob2 interface [BITS],GetNotifyCmdLine method, IBackgroundCopyJob2.GetNotifyCmdLine, IBackgroundCopyJob2::GetNotifyCmdLine, _drz_ibackgroundcopyjob2_getnotifycmdline, bits.ibackgroundcopyjob2_getnotifycmdline, bits1_5/IBackgroundCopyJob2::GetNotifyCmdLine
ms.topic: method
req.header: bits1_5.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits1_5.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: BitsPrx2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.GetNotifyCmdLine
product: Windows
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
---

# IBackgroundCopyJob2::GetNotifyCmdLine


## -description


Retrieves the program to execute when the job enters the error or transferred state.


## -parameters




### -param pProgram [out]

Null-terminated string that contains the program to execute when the job enters the error or transferred state. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>pProgram</i> when done.


### -param pParameters [out]

Null-terminated string that contains the arguments of the program in <i>pProgram</i>. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>pParameters</i> when done.


## -returns



This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.




## -remarks



The 
<b>GetNotifyCmdLine</b> method sets <i>pProgram</i> and <i>pParameters</i> to an empty string (L"") if the 
<a href="https://msdn.microsoft.com/61b99d01-ca0f-4a89-b7ca-77d23c21a9ad">IBackgroundCopyJob2::SetNotifyCmdLine</a> method has not been called.




## -see-also




<a href="https://msdn.microsoft.com/61b99d01-ca0f-4a89-b7ca-77d23c21a9ad">IBackgroundCopyJob2::SetNotifyCmdLine</a>
 

 

