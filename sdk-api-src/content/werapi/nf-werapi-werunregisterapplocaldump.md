---
UID: NF:werapi.WerUnregisterAppLocalDump
title: WerUnregisterAppLocalDump function
author: windows-sdk-content
description: Cancels the registration that was made by calling the WerRegisterAppLocalDump function to specify that Windows Error Reporting (WER) should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding.
old-location: wer\werunregisterapplocaldump.htm
old-project: wer
ms.assetid: A3AD976A-9C44-494C-ABF0-90D151001E30
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WerUnregisterAppLocalDump, WerUnregisterAppLocalDump function [Windows Error Reporting], wer.werunregisterapplocaldump, werapi/WerUnregisterAppLocalDump
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: KernelBase.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerUnregisterAppLocalDump function


## -description


Cancels the registration that was made by calling the <a href="https://msdn.microsoft.com/C57F5758-2BF7-444E-A22C-62C925B899A1">WerRegisterAppLocalDump</a> function to specify that Windows Error Reporting (WER) should  save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C57F5758-2BF7-444E-A22C-62C925B899A1">WerRegisterAppLocalDump</a>
 

 

