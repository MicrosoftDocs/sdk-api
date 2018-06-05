---
UID: NF:amsi.AmsiCloseSession
title: AmsiCloseSession function
author: windows-sdk-content
description: Close a session that was opened by AmsiOpenSession.
old-location: amsi\amsiclosesession.htm
old-project: AMSI
ms.assetid: 1DF760A2-22AE-427E-8395-1EE34BD7BCAB
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: AmsiCloseSession, AmsiCloseSession function [Antimalware Scan Interface], amsi.amsiclosesession, amsi/AmsiCloseSession
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	amsi.dll
api_name:
-	AmsiCloseSession
product: Windows
targetos: Windows
req.lib: Amsi.lib
req.dll: Amsi.dll
req.irql: 
---

# AmsiCloseSession function


## -description


Close a session that was opened by <a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>.


## -parameters




### -param amsiContext [in]

The handle of type HAMSICONTEXT that was initially received from <a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>.


### -param amsiSession

TBD




#### - session [in]

The handle of type HAMSISESSION that was initially received from <a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/946FC79C-556C-404E-A559-323AA69B3EC6">AmsiInitialize</a>



<a href="https://msdn.microsoft.com/588C9003-8689-4D1C-BDFB-386E60BAECD5">AmsiOpenSession</a>
 

 

