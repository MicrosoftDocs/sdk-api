---
UID: NF:werapi.WerUnregisterAppLocalDump
title: WerUnregisterAppLocalDump function (werapi.h)
description: Cancels the registration that was made by calling the WerRegisterAppLocalDump function to specify that Windows Error Reporting (WER) should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding.
helpviewer_keywords: ["WerUnregisterAppLocalDump","WerUnregisterAppLocalDump function [Windows Error Reporting]","wer.werunregisterapplocaldump","werapi/WerUnregisterAppLocalDump"]
old-location: wer\werunregisterapplocaldump.htm
tech.root: wer
ms.assetid: A3AD976A-9C44-494C-ABF0-90D151001E30
ms.date: 12/05/2018
ms.keywords: WerUnregisterAppLocalDump, WerUnregisterAppLocalDump function [Windows Error Reporting], wer.werunregisterapplocaldump, werapi/WerUnregisterAppLocalDump
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: KernelBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerUnregisterAppLocalDump
 - werapi/WerUnregisterAppLocalDump
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KernelBase.dll
 - Kernel32.dll
 - Api-ms-win-core-windowserrorreporting-l1.dll
api_name:
 - WerUnregisterAppLocalDump
---

# WerUnregisterAppLocalDump function


## -description

Cancels the registration that was made by calling the <a href="/windows/desktop/api/werapi/nf-werapi-werregisterapplocaldump">WerRegisterAppLocalDump</a> function to specify that Windows Error Reporting (WER) should  save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding.



## -returns

If this function succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -see-also

<a href="/windows/desktop/api/werapi/nf-werapi-werregisterapplocaldump">WerRegisterAppLocalDump</a>
