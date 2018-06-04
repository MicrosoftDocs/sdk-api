---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PFN_WdsCliCallback callback function


## -description


Defines a callback function that WDS can call for progress notification and error messages during a 
    file or image transfer.


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
      <a href="https://msdn.microsoft.com/43590cee-20d5-47da-8e35-fa4fda1da175">WdsCliTransferImage</a> or 
      <a href="https://msdn.microsoft.com/d219b7ee-4cb8-43ce-959b-4793c7df17ff">WdsCliTransferFile</a> function.


### -param lParam [in, optional]

The meaning of the value contained by this parameter depends upon the 
      <i>dwMessageId</i> parameter.


### -param pvUserData [in, optional]

A pointer to optional user information attached to this session by the 
      <a href="https://msdn.microsoft.com/43590cee-20d5-47da-8e35-fa4fda1da175">WdsCliTransferImage</a> or 
      <a href="https://msdn.microsoft.com/d219b7ee-4cb8-43ce-959b-4793c7df17ff">WdsCliTransferFile</a> function.


## -returns



This callback function does not return a value.




## -remarks



A callback function can call the 
    <a href="https://msdn.microsoft.com/8d138b95-4be1-4f53-ac15-21503408954b">WdsCliCancelTransfer</a> function to cancel a 
    transfer. Although a callback function can also call the 
    <a href="https://msdn.microsoft.com/2328ce69-5a2d-4c4e-bf24-95a379fb7faa">WdsCliWaitForTransfer</a> function, this is not 
    recommended because no additional callbacks will be received until the current callback is unblocked.



