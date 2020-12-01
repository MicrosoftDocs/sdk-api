---
UID: NC:wdsclientapi.PFN_WdsCliCallback
title: PFN_WdsCliCallback (wdsclientapi.h)
description: Defines a callback function that WDS can call for progress notification and error messages during a file or image transfer.
helpviewer_keywords: ["PFN_WdsCliCallback","PFN_WdsCliCallback callback","PFN_WdsCliCallback callback function [Windows Deployment Services]","WDS_CLI_MSG_COMPLETE","WDS_CLI_MSG_PROGRESS","WDS_CLI_MSG_START","WDS_CLI_MSG_TEXT","wds.pfn_wdsclicallback","wdsclientapi/PFN_WdsCliCallback"]
old-location: wds\pfn_wdsclicallback.htm
tech.root: wds
ms.assetid: b071ba1c-5860-4492-ad86-71eaeeb74df4
ms.date: 12/05/2018
ms.keywords: PFN_WdsCliCallback, PFN_WdsCliCallback callback, PFN_WdsCliCallback callback function [Windows Deployment Services], WDS_CLI_MSG_COMPLETE, WDS_CLI_MSG_PROGRESS, WDS_CLI_MSG_START, WDS_CLI_MSG_TEXT, wds.pfn_wdsclicallback, wdsclientapi/PFN_WdsCliCallback
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_WdsCliCallback
 - wdsclientapi/PFN_WdsCliCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WdsClientAPI.h
api_name:
 - PFN_WdsCliCallback
---

## -description

Defines a callback function that WDS can call for progress notification and error messages during a file or image transfer.

## -parameters

### -param dwMessageId [in]

The type of message and the meaning of the <i>lParam</i> parameter.

This parameter can have only one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDS_CLI_MSG_START"></a><a id="wds_cli_msg_start"></a><dl>
<dt><b>WDS_CLI_MSG_START</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The transfer start message. The <i>lParam</i> parameter is a pointer to a 
        <b>LARGE_INTEGER</b> value containing the file size of the transfer.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_CLI_MSG_COMPLETE"></a><a id="wds_cli_msg_complete"></a><dl>
<dt><b>WDS_CLI_MSG_COMPLETE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The transfer complete message. The <i>lParam</i> parameter is an 
        <b>HRESULT</b> value.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_CLI_MSG_PROGRESS"></a><a id="wds_cli_msg_progress"></a><dl>
<dt><b>WDS_CLI_MSG_PROGRESS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The transfer progress message. The <i>lParam</i> parameter is a 
        <b>ULONG</b> value that is the percentage of transfer completed.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_CLI_MSG_TEXT"></a><a id="wds_cli_msg_text"></a><dl>
<dt><b>WDS_CLI_MSG_TEXT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The informational message. The <i>lParam</i> parameter is pointer to a debugging string that 
        can be used for diagnostic purposes.

</td>
</tr>
</table>

### -param wParam [in, optional]

This message parameter should always be set to the value of the transfer handle returned by the 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferimage">WdsCliTransferImage</a> or 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferfile">WdsCliTransferFile</a> function.

### -param lParam [in, optional]

The meaning of the value contained by this parameter depends upon the 
      <i>dwMessageId</i> parameter.

### -param pvUserData [in, optional]

A pointer to optional user information attached to this session by the 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferimage">WdsCliTransferImage</a> or 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclitransferfile">WdsCliTransferFile</a> function.

## -remarks

A callback function can call the 
    <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicanceltransfer">WdsCliCancelTransfer</a> function to cancel a 
    transfer. Although a callback function can also call the 
    <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliwaitfortransfer">WdsCliWaitForTransfer</a> function, this is not 
    recommended because no additional callbacks will be received until the current callback is unblocked.