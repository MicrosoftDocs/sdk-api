---
UID: NF:resapi.ResUtilSetValueEx
title: ResUtilSetValueEx function
author: windows-driver-content
description: Sets a value in the cluster database.
old-location: mscs\resutilsetvalueex.htm
old-project: MsCS
ms.assetid: AE0D9AF5-3161-453F-95FC-C759640AF58B
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ResUtilSetValueEx, ResUtilSetValueEx function [Failover Cluster], mscs.resutilsetvalueex, resapi/ResUtilSetValueEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RESOURCE_EXIT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ResUtils.dll
api_name:
-	ResUtilSetValueEx
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ResUtilSetValueEx function


## -description


Sets a value in the  <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.


## -parameters




### -param hkeyClusterKey [in]

A key that identifies the location of the value in the cluster database.


### -param valueName [in]

A Null-terminated Unicode string that contains the name of the value to update.


### -param valueType [in]

A flag that indicates the type of the value to update.


### -param valueData [in]

A pointer to the new data for the value.


### -param valueSize [in]

The size of the new value, in bytes.


### -param flags [in]

The flags that specify settings for the operation.


## -returns



Returns <b>ERROR_SUCCESS</b> if the operation succeeds; otherwise, returns a system error code.



