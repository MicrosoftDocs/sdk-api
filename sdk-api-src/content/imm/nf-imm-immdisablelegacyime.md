---
UID: NF:imm.ImmDisableLegacyIME
title: ImmDisableLegacyIME function
author: windows-sdk-content
description: Indicates that this thread is a Windows Store app&#32;UI thread.
old-location: intl\immdisablelegacyime.htm
tech.root: Intl
ms.assetid: 5B207438-B437-45B0-AE0C-DDB1B19488F2
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMMDisableLegacyIME, IMMDisableLegacyIME function [Internationalization for Windows Applications], ImmDisableLegacyIME, imm/IMMDisableLegacyIME, intl.immdisablelegacyime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - imm32.dll
api_name:
 - IMMDisableLegacyIME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImmDisableLegacyIME
: 
---

# ImmDisableLegacyIME function


## -description


Indicates that this thread is a Windows Store app UI thread.


## -parameters






## -returns



Returns <b>TRUE</b> if successful;   otherwise, <b>FALSE</b>. 




## -remarks



Windows Store app brokers such as explorer.exe should call this function in Windows Store app UI threads to ensure that only IMEs that are compatible with  Windows Store apps are made available.  Those Windows Store app threads that don't require IME input should call <a href="https://msdn.microsoft.com/c563fc24-3c56-40ac-8539-8336d5231537">ImmDisableIME</a> to disable IMM entirely for that thread.

The app must call this function before the first top-level window in the thread receives the <a href="https://msdn.microsoft.com/en-us/library/ms632619(v=VS.85).aspx">WM_CREATE</a> message. Thus, the app must call this function in one of the following places:

<ul>
<li>Any time before  <a href="https://msdn.microsoft.com/en-us/library/ms632679(v=VS.85).aspx">CreateWindow</a> is called to create the first top-level window.</li>
<li>In the <a href="https://msdn.microsoft.com/en-us/library/ms632635(v=VS.85).aspx">WM_NCCREATE</a> handler for the first top-level window.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

