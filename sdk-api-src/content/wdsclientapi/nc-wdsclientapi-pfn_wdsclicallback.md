---
UID: NC:wdsclientapi.PFN_WdsCliCallback
title: PFN_WdsCliCallback
author: windows-sdk-content
description: Defines a callback function that WDS can call for progress notification and error messages during a file or image transfer.
old-location: wds\pfn_wdsclicallback.htm
old-project: Wds
ms.assetid: b071ba1c-5860-4492-ad86-71eaeeb74df4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: PFN_WdsCliCallback, PFN_WdsCliCallback callback, PFN_WdsCliCallback callback function [Windows Deployment Services], WDS_CLI_MSG_COMPLETE, WDS_CLI_MSG_PROGRESS, WDS_CLI_MSG_START, WDS_CLI_MSG_TEXT, wds.pfn_wdsclicallback, wdsclientapi/PFN_WdsCliCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: WAITCHAIN_NODE_INFO, *PWAITCHAIN_NODE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	WdsClientAPI.h
api_name:
-	PFN_WdsCliCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



