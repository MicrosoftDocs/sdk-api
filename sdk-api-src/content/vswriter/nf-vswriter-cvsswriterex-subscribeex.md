---
UID: NF:vswriter.CVssWriterEx.SubscribeEx
title: CVssWriterEx::SubscribeEx
author: windows-sdk-content
description: Causes the writer to subscribe to VSS events.
old-location: base\cvsswriterex_subscribeex.htm
tech.root: VSS
ms.assetid: b60ca619-c92b-4700-a048-7c74fad3d0e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CVssWriterEx interface,SubscribeEx method, CVssWriterEx.SubscribeEx, CVssWriterEx::SubscribeEx, SubscribeEx, SubscribeEx method, SubscribeEx method,CVssWriterEx interface, base.cvsswriterex_subscribeex, vswriter/CVssWriterEx::SubscribeEx
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriterEx.SubscribeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriterEx::SubscribeEx


## -description


Causes the writer to subscribe to VSS events.


## -parameters




### -param dwUnsubscribeTimeout [in]

The length of time, in milliseconds, that the method will wait before timing out.


### -param dwEventFlags [in]

A bitmask of 
<a href="https://msdn.microsoft.com/4aa3afe4-98da-4376-b795-75bf404aaed9">VSS_SUBSCRIBE_MASK</a> values indicating the events that VSS should notify the writer about. 




The default value for this argument is (<b>VSS_SM_BACKUP_EVENTS_FLAG</b> | <b>VSS_SM_RESTORE_EVENTS_FLAG</b>). Currently, the caller should not override the default value.

This parameter is reserved for future use.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The writer has successfully subscribed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_WRITER_ALREADY_SUBSCRIBED</b></dt>
</dl>
</td>
<td width="60%">
The writer has previously called this method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ab9520c9-bd6b-4c81-87fc-f5cda6ee9c94">CVssWriter::Subscribe</a>



<a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a>
 

 

