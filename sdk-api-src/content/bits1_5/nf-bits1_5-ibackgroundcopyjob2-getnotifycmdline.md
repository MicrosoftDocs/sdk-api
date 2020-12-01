---
UID: NF:bits1_5.IBackgroundCopyJob2.GetNotifyCmdLine
title: IBackgroundCopyJob2::GetNotifyCmdLine
description: Retrieves the program to execute when the job enters the error or transferred state.
helpviewer_keywords: ["GetNotifyCmdLine","GetNotifyCmdLine method [BITS]","GetNotifyCmdLine method [BITS]","IBackgroundCopyJob2 interface","IBackgroundCopyJob2 interface [BITS]","GetNotifyCmdLine method","IBackgroundCopyJob2.GetNotifyCmdLine","IBackgroundCopyJob2::GetNotifyCmdLine","_drz_ibackgroundcopyjob2_getnotifycmdline","bits.ibackgroundcopyjob2_getnotifycmdline","bits1_5/IBackgroundCopyJob2::GetNotifyCmdLine"]
old-location: bits\ibackgroundcopyjob2_getnotifycmdline.htm
tech.root: Bits
ms.assetid: 62978315-e893-4617-8e6d-63bab8204913
ms.date: 12/05/2018
ms.keywords: GetNotifyCmdLine, GetNotifyCmdLine method [BITS], GetNotifyCmdLine method [BITS],IBackgroundCopyJob2 interface, IBackgroundCopyJob2 interface [BITS],GetNotifyCmdLine method, IBackgroundCopyJob2.GetNotifyCmdLine, IBackgroundCopyJob2::GetNotifyCmdLine, _drz_ibackgroundcopyjob2_getnotifycmdline, bits.ibackgroundcopyjob2_getnotifycmdline, bits1_5/IBackgroundCopyJob2::GetNotifyCmdLine
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
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob2::GetNotifyCmdLine
 - bits1_5/IBackgroundCopyJob2::GetNotifyCmdLine
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsPrx2.dll
api_name:
 - IBackgroundCopyJob2.GetNotifyCmdLine
---

# IBackgroundCopyJob2::GetNotifyCmdLine


## -description

Retrieves the program to execute when the job enters the error or transferred state.

## -parameters

### -param pProgram [out]

Null-terminated string that contains the program to execute when the job enters the error or transferred state. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>pProgram</i> when done.

### -param pParameters [out]

Null-terminated string that contains the arguments of the program in <i>pProgram</i>. Call the 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>pParameters</i> when done.

## -returns

This method returns <b>S_OK</b> on success or one of the standard COM <b>HRESULT</b> values on error.

## -remarks

The 
<b>GetNotifyCmdLine</b> method sets <i>pProgram</i> and <i>pParameters</i> to an empty string (L"") if the 
<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a> method has not been called.

## -see-also

<a href="/windows/desktop/api/bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline">IBackgroundCopyJob2::SetNotifyCmdLine</a>