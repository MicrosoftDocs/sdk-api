---
UID: NF:amsi.AmsiCloseSession
title: AmsiCloseSession function (amsi.h)
author: windows-sdk-content
description: Close a session that was opened by AmsiOpenSession.
old-location: amsi\amsiclosesession.htm
tech.root: AMSI
ms.assetid: 1DF760A2-22AE-427E-8395-1EE34BD7BCAB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AmsiCloseSession, AmsiCloseSession function [Antimalware Scan Interface], amsi.amsiclosesession, amsi/AmsiCloseSession
ms.topic: function
f1_keywords: 
 - "amsi/AmsiCloseSession"
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
 - AmsiCloseSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AmsiCloseSession function


## -description


Close a session that was opened by <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>.


### -param amsiSession [in]

The handle of type HAMSISESSION that was initially received from <a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiinitialize">AmsiInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amsi/nf-amsi-amsiopensession">AmsiOpenSession</a>
 

 

