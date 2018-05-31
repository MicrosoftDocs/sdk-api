---
UID: NF:tdh.TdhLoadManifest
title: TdhLoadManifest function
author: windows-sdk-content
description: Loads the manifest used to decode a log file.
old-location: etw\tdhloadmanifest.htm
old-project: ETW
ms.assetid: 85dfcf73-ea3a-47e2-ad1a-3891b3917ecf
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: TdhLoadManifest, TdhLoadManifest function [ETW], etw.tdhloadmanifest, tdh/TdhLoadManifest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TEMPLATE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tdh.dll
-	API-MS-Win-Eventing-Tdh-L1-1-0.dll
-	MinTdh.dll
api_name:
-	TdhLoadManifest
product: Windows
targetos: Windows
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TdhLoadManifest function


## -description


Loads the manifest used to decode a log file.


## -parameters




### -param Manifest [in]

The full path to the manifest.


## -returns



Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The manifest file was not found at the specified path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Manifest</i> parameter cannot be <b>NULL</b> and the path cannot exceed MAX_PATH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_XML_PARSE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The manifest did not pass validation. To determine the validation errors, run the manifest through the message compiler (mc.exe).

</td>
</tr>
</table>
 




## -remarks



To consume events, TDH requires the provider's manifest. Typically, you decode the log file on a computer that contains the provider. Since the provider includes the mainifest as a resource, TDH uses the provider to get the manifest. To decode the log file on a computer that does not contain the provider, you must first use the  TraceRpt.exe executable to export the manifest (see the –export switch) from the provider on a computer that does contain the provider. After you have the manifest file, you can decode the log file on a computer that does not contain the provider.

You need to call this function before decoding the first event. For example, you can call this function before calling the <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> function. After processing all the events, call the <a href="https://msdn.microsoft.com/ce0dd781-04b2-4e0c-9e79-44864f53f176">TdhUnloadManifest</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ce0dd781-04b2-4e0c-9e79-44864f53f176">TdhUnloadManifest</a>
 

 

