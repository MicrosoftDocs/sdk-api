---
UID: NF:wdsclientapi.WdsCliTransferFile
title: WdsCliTransferFile function (wdsclientapi.h)
description: Transfers a file from a WDS server to the WDS client using a multicast transfer protocol.
helpviewer_keywords: ["WDS_CLI_TRANSFER_ASYNCHRONOUS","WdsCliTransferFile","WdsCliTransferFile function [Windows Deployment Services]","wds.wdsclitransferfile","wdsclientapi/WdsCliTransferFile"]
old-location: wds\wdsclitransferfile.htm
tech.root: wds
ms.assetid: d219b7ee-4cb8-43ce-959b-4793c7df17ff
ms.date: 12/05/2018
ms.keywords: WDS_CLI_TRANSFER_ASYNCHRONOUS, WdsCliTransferFile, WdsCliTransferFile function [Windows Deployment Services], wds.wdsclitransferfile, wdsclientapi/WdsCliTransferFile
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliTransferFile
 - wdsclientapi/WdsCliTransferFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliTransferFile
---

# WdsCliTransferFile function


## -description

Transfers a file from a WDS server to the WDS client using a multicast transfer protocol.

## -parameters

### -param pwszServer [in]

A pointer to a null-terminated string value that contains the  WDS server name.

### -param pwszNamespace [in]

A pointer to a null-terminated string value that contains the multicast namespace name for the image.

### -param pwszRemoteFilePath [in]

A pointer to a null-terminated string value that contains the  full path for the remote location from which to copy the file being transferred.

### -param pwszLocalFilePath [in]

A pointer to a null-terminated string value that contains the full path to the local location to store the file being transferred.

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

A pointer to an optional callback function for this transfer.

### -param pvUserData [in, optional]

A pointer to optional user information that can be passed to the callback function.

### -param phTransfer [out]

A pointer to a transfer handle that can be used with the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliwaitfortransfer">WdsCliWaitForTransfer</a> or <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicanceltransfer">WdsCliCancelTransfer</a> functions to wait for the transfer to complete or to cancel the transfer.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

Call the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function to close the handle returned by this function.