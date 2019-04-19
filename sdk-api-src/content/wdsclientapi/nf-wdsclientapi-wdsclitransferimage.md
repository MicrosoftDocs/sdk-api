---
UID: NF:wdsclientapi.WdsCliTransferImage
title: WdsCliTransferImage function (wdsclientapi.h)
author: windows-sdk-content
description: Transfers an image from a WDS server to the WDS client.
old-location: wds\wdsclitransferimage.htm
tech.root: wds
ms.assetid: 43590cee-20d5-47da-8e35-fa4fda1da175
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WDS_CLI_TRANSFER_ASYNCHRONOUS, WdsCliTransferImage, WdsCliTransferImage function [Windows Deployment Services], wds.wdsclitransferimage, wdsclientapi/WdsCliTransferImage
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
 - WdsCliTransferImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliTransferImage function


## -description


Transfers an image from a WDS server to the WDS client. 


## -parameters




### -param hImage [in]

A WDS image handle that refers to a remote image.


### -param pwszLocalPath [in]

A pointer to a null-terminated string value that contains the full path to the local location to store the image file being transferred.


### -param dwFlags [in]

Options associated with the file transfer.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDS_CLI_TRANSFER_ASYNCHRONOUS"></a><a id="wds_cli_transfer_asynchronous"></a><dl>
<dt><b>WDS_CLI_TRANSFER_ASYNCHRONOUS</b></dt>
</dl>
</td>
<td width="60%">
This flag specifies an asynchronous transfer.

</td>
</tr>
</table>
 


### -param dwReserved [in]

This parameter is reserved.


### -param pfnWdsCliCallback [in, optional]

A pointer to an optional callback function that will receive callbacks for this transfer.


### -param pvUserData [in, optional]

A pointer to optional user information that can be passed to the callback function.


### -param phTransfer [out]

A pointer to a transfer handle that can be used with the <a href="https://msdn.microsoft.com/2328ce69-5a2d-4c4e-bf24-95a379fb7faa">WdsCliWaitForTransfer</a> or <a href="https://msdn.microsoft.com/8d138b95-4be1-4f53-ac15-21503408954b">WdsCliCancelTransfer</a> functions to wait for the transfer to complete or to cancel the transfer.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



Call the <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function to close the handle returned by this function.



