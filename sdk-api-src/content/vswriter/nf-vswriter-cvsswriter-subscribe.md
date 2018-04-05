---
UID: NF:vswriter.CVssWriter.Subscribe
title: CVssWriter::Subscribe method
author: windows-driver-content
description: The Subscribe method subscribes the writer with VSS.
old-location: base\cvsswriter_subscribe.htm
old-project: VSS
ms.assetid: ab9520c9-bd6b-4c81-87fc-f5cda6ee9c94
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CVssWriter, CVssWriter interface [VSS], Subscribe method, CVssWriter::Subscribe, Subscribe method [VSS], Subscribe method [VSS], CVssWriter interface, Subscribe,CVssWriter.Subscribe, _win32_cvsswriter_subscribe, base.cvsswriter_subscribe, vswriter/CVssWriter::Subscribe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	CVssWriter.Subscribe
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# CVssWriter::Subscribe method


## -description


The 
<b>Subscribe</b> method subscribes the writer with VSS.

<b>Subscribe</b> is a public method implemented by the base class.


## -parameters






#### - dwEventFlags [in]

A bit mask (or bitwise OR) of 
<a href="https://msdn.microsoft.com/4aa3afe4-98da-4376-b795-75bf404aaed9">VSS_SUBSCRIBE_MASK</a> values indicating the events that VSS should notify the writer about. 




The default value for this argument is (VSS_SM_BACKUP_EVENTS_FLAG | VSS_SM_RESTORE_EVENTS_FLAG). Currently, the caller should not override the default value.

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
Successfully subscribed the writer object.

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




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>



<a href="https://msdn.microsoft.com/b2bb68d1-7beb-4ba1-b16d-6314ac3f4a3d">CVssWriter::Unsubscribe</a>



<a href="https://msdn.microsoft.com/4aa3afe4-98da-4376-b795-75bf404aaed9">VSS_SUBSCRIBE_MASK</a>
 

 

