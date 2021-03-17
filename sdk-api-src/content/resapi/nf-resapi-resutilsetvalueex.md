---
UID: NF:resapi.ResUtilSetValueEx
title: ResUtilSetValueEx function (resapi.h)
description: Sets a value in the cluster database.
helpviewer_keywords: ["ResUtilSetValueEx","ResUtilSetValueEx function [Failover Cluster]","mscs.resutilsetvalueex","resapi/ResUtilSetValueEx"]
old-location: mscs\resutilsetvalueex.htm
tech.root: MsCS
ms.assetid: AE0D9AF5-3161-453F-95FC-C759640AF58B
ms.date: 12/05/2018
ms.keywords: ResUtilSetValueEx, ResUtilSetValueEx function [Failover Cluster], mscs.resutilsetvalueex, resapi/ResUtilSetValueEx
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilSetValueEx
 - resapi/ResUtilSetValueEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilSetValueEx
---

# ResUtilSetValueEx function


## -description

Sets a value in the  <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a>.

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