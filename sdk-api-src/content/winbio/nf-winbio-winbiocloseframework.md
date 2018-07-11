---
UID: NF:winbio.WinBioCloseFramework
title: WinBioCloseFramework function
author: windows-sdk-content
description: Closes a framework handle previously opened with WinBioAsyncOpenFramework. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbiocloseframework.htm
old-project: secbiomet
ms.assetid: AE13FB2F-0B6B-4D98-A75A-E8A2EA525136
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: WinBioCloseFramework, WinBioCloseFramework function [Windows Biometric Framework API], secbiomet.winbiocloseframework, winbio/WinBioCloseFramework
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioCloseFramework
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioCloseFramework function


## -description


Closes a framework handle previously opened with <a href="https://msdn.microsoft.com/D9557A6F-32C4-464F-8800-6E546808F100">WinBioAsyncOpenFramework</a>. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param FrameworkHandle [in]

Handle to the framework session that will be closed.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




## -remarks



This function never blocks.



