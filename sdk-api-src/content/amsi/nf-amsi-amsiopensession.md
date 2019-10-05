---
UID: NF:amsi.AmsiOpenSession
title: AmsiOpenSession function (amsi.h)
author: windows-sdk-content
description: Opens a session within which multiple scan requests can be correlated.
old-location: amsi\amsiopensession.htm
tech.root: AMSI
ms.assetid: 588C9003-8689-4D1C-BDFB-386E60BAECD5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AmsiOpenSession, AmsiOpenSession function [Antimalware Scan Interface], amsi.amsiopensession, amsi/AmsiOpenSession
ms.topic: function
f1_keywords: 
 - "amsi/AmsiOpenSession"
dev_langs:
 - c++
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
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - amsi.dll
api_name:
 - AmsiOpenSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AmsiOpenSession function


## -description


Opens a session within which multiple scan requests can be correlated.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.


### -param amsiSession [out]

A handle of type HAMSISESSION that must be passed to all subsequent calls to the AMSI API within the session.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the app is finished with the session it must call <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiclosesession">AmsiCloseSession</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiclosesession">AmsiCloseSession</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>
 

 

