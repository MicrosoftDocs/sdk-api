---
UID: NF:wdsclientapi.WdsCliLog
title: WdsCliLog function
author: windows-sdk-content
description: Sends a log event to the WDS server.
old-location: wds\wdsclilog.htm
tech.root: wds
ms.assetid: c4b183c7-5118-4752-a3a4-ef594f133288
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WDS_LOG_LEVEL_DISABLED, WDS_LOG_LEVEL_ERROR, WDS_LOG_LEVEL_INFO, WDS_LOG_LEVEL_WARNING, WDS_LOG_TYPE_CLIENT_APPLY_FINISHED, WDS_LOG_TYPE_CLIENT_APPLY_STARTED, WDS_LOG_TYPE_CLIENT_ERROR, WDS_LOG_TYPE_CLIENT_FINISHED, WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE, WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED, WDS_LOG_TYPE_CLIENT_MAX_CODE, WDS_LOG_TYPE_CLIENT_STARTED, WdsCliLog, WdsCliLog function [Windows Deployment Services], wds.wdsclilog, wdsclientapi/WdsCliLog
ms.topic: function
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - WdsCliLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsCliLog function


## -description


Sends a log event to the WDS server.


## -parameters




### -param hSession [in]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a> function.


### -param ulLogLevel [in]

Indicates the threshold severity required to log an event. The WDS server will log events only if the server log level is greater 
      than or equal to the value specified.


This parameter can have one of the following values.





#### WDS_LOG_LEVEL_DISABLED (0)



#### WDS_LOG_LEVEL_ERROR (1)



#### WDS_LOG_LEVEL_WARNING (2)



#### WDS_LOG_LEVEL_INFO (3)


### -param ulMessageCode [in]

The type of message that is being logged.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_ERROR"></a><a id="wds_log_type_client_error"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_ERROR</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A client error message. An additional parameter of type <b>PWSTR</b> that describes the error is 
        required.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_STARTED"></a><a id="wds_log_type_client_started"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_STARTED</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A client started message. No additional parameters are required.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_FINISHED"></a><a id="wds_log_type_client_finished"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_FINISHED</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A client finished message. No additional parameters are required.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED"></a><a id="wds_log_type_client_image_selected"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
A client image selected message. Two additional parameters of type <b>PWSTR</b> are required. The first is the Image 
        Name and the second is the Group Name.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_APPLY_STARTED"></a><a id="wds_log_type_client_apply_started"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_APPLY_STARTED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
No additional parameters are required.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_APPLY_FINISHED"></a><a id="wds_log_type_client_apply_finished"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_APPLY_FINISHED</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
No additional parameters are required.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE"></a><a id="wds_log_type_client_generic_message"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
A generic message. An additional parameter of type <b>PWSTR</b> that contains the message is 
        required.

</td>
</tr>
<tr>
<td width="40%"><a id="WDS_LOG_TYPE_CLIENT_MAX_CODE"></a><a id="wds_log_type_client_max_code"></a><dl>
<dt><b>WDS_LOG_TYPE_CLIENT_MAX_CODE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Used to determine an out-of-range index. Values greater than or equal to 
        <b>WDS_LOG_TYPE_CLIENT_MAX_CODE</b> are not valid.

</td>
</tr>
</table>
 


### -param arg4

The quantity and type of the additional arguments varies with the value of the 
      <i>ulMessageCode</i> parameter.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a>



<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

