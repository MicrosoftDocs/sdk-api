---
UID: NF:cfapi.CfExecute
title: CfExecute function
author: windows-sdk-content
description: The main entry point for all connection key based placeholder operations. It is intended to be used by a sync provider to respond to various callbacks from the platform.
old-location: cloudapi\cfexecute.htm
tech.root: cfApi
ms.assetid: 6AC8958D-B060-4468-9811-9BAB0E6A06D3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CfExecute, CfExecute function, cfapi/CfExecute, cloudApi.cfexecute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfExecute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CfExecute function


## -description


The main entry point for all connection key based placeholder operations. It is intended to be used by a sync provider to respond to various callbacks from the platform.


## -parameters




### -param OpInfo [in]

Information about an operation on a placeholder.


### -param OpParams [in, out]

Parameters of an operation on a placeholder.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A valid call to <b>CfExecute</b> will reset the timers of all pending callback requests that belong to the same sync provider process. 


<b>CfExecute</b> takes two variable-sized arguments, i.e., <a href="https://msdn.microsoft.com/4AE9A968-1325-4EFF-8F5B-8F465740B0C4">CF_OPERATION_INFO</a> and <a href="https://msdn.microsoft.com/668C682E-47C2-41BC-A4F9-AA2F2B516F54">CF_OPERATION_PARAMETERS</a>, with one identifying the operation type and the other supplying detailed operation parameters.
Both arguments start with a <b>StructSize</b> field at the beginning of the corresponding structures. Callers of <b>CfExecute</b> are responsible for accurate accounting of the structure size.



