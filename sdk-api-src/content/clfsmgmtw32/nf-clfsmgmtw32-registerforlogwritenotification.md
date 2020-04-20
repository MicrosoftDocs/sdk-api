---
UID: NF:clfsmgmtw32.RegisterForLogWriteNotification
title: RegisterForLogWriteNotification function (clfsmgmtw32.h)
description: The RegisterForLogWriteNotification function is called by a managed log client to enable or disable log write notifications.helpviewer_keywords: ["RegisterForLogWriteNotification","RegisterForLogWriteNotification function [Files]","clfsmgmtw32/RegisterForLogWriteNotification","fs.registerforlogwritenotification"]
old-location: fs\registerforlogwritenotification.htm
tech.root: Clfs
ms.assetid: 08e197af-d88e-46dd-b862-66eb0ab27551
ms.date: 12/05/2018
ms.keywords: RegisterForLogWriteNotification, RegisterForLogWriteNotification function [Files], clfsmgmtw32/RegisterForLogWriteNotification, fs.registerforlogwritenotification
f1_keywords:
- clfsmgmtw32/RegisterForLogWriteNotification
dev_langs:
- c++
req.header: clfsmgmtw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ClfsW32.lib
req.dll: ClfsW32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClfsW32.dll
api_name:
- RegisterForLogWriteNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegisterForLogWriteNotification function


## -description


The <b>RegisterForLogWriteNotification</b> function is 
    called by a managed log client to enable or disable log write notifications.


## -parameters




### -param hLog [in]

A handle to the log on which to resolve the log full condition.


### -param cbThreshold [in]

Number of bytes to be written to the log file before the notification is sent.


### -param fEnable [in]

If <b>TRUE</b>, the notification is enabled. If <b>FALSE</b>, the notification is disabled.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Valid values include the following:




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/clfs/clfs-management-functions">CLFS Management Functions</a>
 

 

