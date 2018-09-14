---
UID: NF:wdsclientapi.WdsCliGetImageHandleFromTransferHandle
title: WdsCliGetImageHandleFromTransferHandle function
author: windows-sdk-content
description: Returns an image handle from a completed transfer handle. The handle is to the local copy of the image that's been transferred from the server to the client.
old-location: wds\wdscligetimagehandlefromtransferhandle.htm
tech.root: wds
ms.assetid: d2356f34-9ef8-4d7d-bb01-843d1aa1cbed
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WdsCliGetImageHandleFromTransferHandle, WdsCliGetImageHandleFromTransferHandle function [Windows Deployment Services], wds.wdscligetimagehandlefromtransferhandle, wdsclientapi/WdsCliGetImageHandleFromTransferHandle
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
 - WdsCliGetImageHandleFromTransferHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliGetImageHandleFromTransferHandle function


## -description


Returns an image handle from a completed transfer handle.  The handle is to the local copy of the image that's been transferred from the server to the client.


## -parameters




### -param hTransfer

A WDS transfer handle that has completed the transfer. This can be the handle returned by the <a href="https://msdn.microsoft.com/43590cee-20d5-47da-8e35-fa4fda1da175">WdsCliTransferImage</a> or <a href="https://msdn.microsoft.com/d219b7ee-4cb8-43ce-959b-4793c7df17ff">WdsCliTransferFile</a> functions.


### -param phImageHandle [out]

A pointer to a location that contains an image handle.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



If the transfer is not yet complete when this function is called, it will return an error code.

Use the <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function to close the image handle returned by this function.



