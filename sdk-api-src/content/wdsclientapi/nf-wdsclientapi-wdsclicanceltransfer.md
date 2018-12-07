---
UID: NF:wdsclientapi.WdsCliCancelTransfer
title: WdsCliCancelTransfer function
author: windows-sdk-content
description: Cancels a WDS transfer operation.
old-location: wds\wdsclicanceltransfer.htm
tech.root: wds
ms.assetid: 8d138b95-4be1-4f53-ac15-21503408954b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WdsCliCancelTransfer, WdsCliCancelTransfer function [Windows Deployment Services], wds.wdsclicanceltransfer, wdsclientapi/WdsCliCancelTransfer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliCancelTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliCancelTransfer function


## -description


Cancels a WDS transfer operation. 


## -parameters




### -param hTransfer [in]

A handle for the WDS transfer operation being canceled. This can be the handle returned by the <a href="https://msdn.microsoft.com/43590cee-20d5-47da-8e35-fa4fda1da175">WdsCliTransferImage</a> or <a href="https://msdn.microsoft.com/d219b7ee-4cb8-43ce-959b-4793c7df17ff">WdsCliTransferFile</a> functions.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This function can be called from a callback function.



