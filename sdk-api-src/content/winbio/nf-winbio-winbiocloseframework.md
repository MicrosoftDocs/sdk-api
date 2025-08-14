---
UID: NF:winbio.WinBioCloseFramework
title: WinBioCloseFramework function (winbio.h)
description: Closes a framework handle previously opened with WinBioAsyncOpenFramework. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioCloseFramework","WinBioCloseFramework function [Windows Biometric Framework API]","secbiomet.winbiocloseframework","winbio/WinBioCloseFramework"]
old-location: secbiomet\winbiocloseframework.htm
tech.root: SecBioMet
ms.assetid: AE13FB2F-0B6B-4D98-A75A-E8A2EA525136
ms.date: 12/05/2018
ms.keywords: WinBioCloseFramework, WinBioCloseFramework function [Windows Biometric Framework API], secbiomet.winbiocloseframework, winbio/WinBioCloseFramework
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioCloseFramework
 - winbio/WinBioCloseFramework
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-biometrics-winbio-core-l1-1-6.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-5.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-4.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-3.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-2.dll
 - Winbio.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioCloseFramework
---

# WinBioCloseFramework function


## -description

Closes a framework handle previously opened with <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopenframework">WinBioAsyncOpenFramework</a>. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param FrameworkHandle [in]

Handle to the framework session that will be closed.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

## -remarks

This function never blocks.