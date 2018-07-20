---
UID: NS:cfapi.CF_OPERATION_INFO
title: CF_OPERATION_INFO
author: windows-sdk-content
description: Information about an operation on a placeholder file or folder.
old-location: cloudapi\cf_operation_info.htm
old-project: cfApi
ms.assetid: 4AE9A968-1325-4EFF-8F5B-8F465740B0C4
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CF_OPERATION_INFO, CF_OPERATION_INFO structure, cfapi/CF_OPERATION_INFO, cloudApi.cf_operation_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CF_OPERATION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_OPERATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CF_OPERATION_INFO structure


## -description


Information about an operation on a placeholder file or folder.


## -struct-fields




### -field StructSize

The size of the structure.


### -field Type

The type of operation performed.


### -field ConnectionKey

A connection key obtained for the communication channel.


### -field TransferKey

An opaque handle to the placeholder.


### -field CorrelationVector

A correlation vector on a placeholder used for telemetry purposes.


### -field SyncStatus

<b>Note</b>  This member is new for Windows 10, version 1803.

The current sync status of the platform. 

The platform queries this information upon any failed operations on a cloud file placeholder. If a structure is available, the platform will use the information provided to construct a more meaningful and actionable message to the user. 
The platform will keep this information on the file until the last handle on it goes away. If <b>null</b>,  the platform will clear the previously set sync status, if there is one. 



### -field RequestKey

 




## -remarks



The platform provides the <b>ConnectionKey</b>, <b>TransferKey</b>, and <b>CorrelationVector</b> to all callback functions registered via <a href="https://msdn.microsoft.com/287DA978-9797-48DF-9C90-BA53BB82475C">CfConnectSyncRoot</a>. Additionally, sync providers can obtain a <b>TransferKey</b> using <a href="https://msdn.microsoft.com/07DDC46A-0C10-4677-A4B0-5A0406BBDAB7">CfGetTransferKey</a> and a <b>CorrelationVector</b> using <a href="https://msdn.microsoft.com/3DB0AAFE-82DC-4707-8DB6-C52D4A9B2771">CfGetCorrelationVector</a>.



