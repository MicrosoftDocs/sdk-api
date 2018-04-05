---
UID: NF:clfsmgmtw32.RegisterForLogWriteNotification
title: RegisterForLogWriteNotification function
author: windows-driver-content
description: The RegisterForLogWriteNotification function is called by a managed log client to enable or disable log write notifications.
old-location: fs\registerforlogwritenotification.htm
old-project: Clfs
ms.assetid: 08e197af-d88e-46dd-b862-66eb0ab27551
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: RegisterForLogWriteNotification, RegisterForLogWriteNotification function [Files], clfsmgmtw32/RegisterForLogWriteNotification, fs.registerforlogwritenotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: CLFS_MGMT_POLICY, *PCLFS_MGMT_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ClfsW32.dll
api_name:
-	RegisterForLogWriteNotification
product: Windows
targetos: Windows
req.lib: ClfsW32.lib
req.dll: ClfsW32.dll
req.irql: 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Valid values include the following:




## -see-also




<a href="https://msdn.microsoft.com/a8bcfdc6-3056-4f82-825b-f224100d87cb">CLFS Management Functions</a>
 

 

