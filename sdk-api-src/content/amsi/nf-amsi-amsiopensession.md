---
UID: NF:amsi.AmsiOpenSession
title: AmsiOpenSession function
author: windows-sdk-content
description: Opens a session within which multiple scan requests can be correlated.
old-location: amsi\amsiopensession.htm
old-project: AMSI
ms.assetid: 588C9003-8689-4D1C-BDFB-386E60BAECD5
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: AmsiOpenSession, AmsiOpenSession function [Antimalware Scan Interface], amsi.amsiopensession, amsi/AmsiOpenSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: amsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiOpenSession
product: Windows
targetos: Windows
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
---

# AmsiOpenSession function


## -description


Opens a session within which multiple scan requests can be correlated.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


### -param amsiSession

TBD




#### - session [out]

A handle of type HAMSISESSION that must be passed to all subsequent calls to the AMSI API within the session.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the app is finished with the session it must call <a href="https://msdn.microsoft.com/1DF760A2-22AE-427E-8395-1EE34BD7BCAB">AmsiCloseSession</a>.




## -see-also




<a href="https://msdn.microsoft.com/1DF760A2-22AE-427E-8395-1EE34BD7BCAB">AmsiCloseSession</a>



<a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>
 

 

