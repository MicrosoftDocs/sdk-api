---
UID: NF:vsbackup.IVssExamineWriterMetadataEx.GetIdentityEx
title: IVssExamineWriterMetadataEx::GetIdentityEx
author: windows-sdk-content
description: The GetIdentityEx method obtains the writer instance name and other basic information about a specific writer instance.
old-location: base\ivssexaminewritermetadataex_getidentityex.htm
tech.root: vss
ms.assetid: f36cfa0e-b51e-488b-89b1-99544e2883d9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIdentityEx, GetIdentityEx method [VSS], GetIdentityEx method [VSS],IVssExamineWriterMetadataEx interface, IVssExamineWriterMetadataEx interface [VSS],GetIdentityEx method, IVssExamineWriterMetadataEx.GetIdentityEx, IVssExamineWriterMetadataEx::GetIdentityEx, base.ivssexaminewritermetadataex_getidentityex, vsbackup/IVssExamineWriterMetadataEx::GetIdentityEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IVssExamineWriterMetadataEx.GetIdentityEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssExamineWriterMetadataEx::GetIdentityEx


## -description


The <b>GetIdentityEx</b> method obtains the writer instance name and other basic information about a specific writer instance.


## -parameters




### -param pidInstance [out]

Globally unique identifier (GUID) of the writer instance.


### -param pidWriter [out]

GUID of the writer class.


### -param pbstrWriterName [out]

Pointer to a string specifying the name of the writer.


### -param pbstrInstanceName [out]

Pointer to a string specifying the writer instance name.


### -param pUsage [out]

Pointer to a 
<a href="https://msdn.microsoft.com/31997417-d993-4f28-b108-ce1dd8239650">VSS_USAGE_TYPE</a> enumeration value indicating how the data managed by the writer is used on the host system.


### -param pSource [out]

Pointer to a 
<a href="https://msdn.microsoft.com/cb89c3cc-5a8e-419e-839c-f72a1886eadf">VSS_SOURCE_TYPE</a> enumeration value indicating the type of data managed by the writer.


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
Successfully returned the identity information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is  not valid. Check the event log for details. For more information, see 
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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
</table>
 




## -remarks



This method is identical to the <a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a> method except for the <i>pbstrInstanceName</i> parameter.

The <i>pbstrInstanceName</i> parameter is the writer instance name that was specified during writer initialization by <a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>.

The writer instance name is useful for writers that support running multiple writer instances with the same writer class ID on a single computer. The writer instance name can be used to identify the specific instance. Therefore, the writer must make the instance name unique within the writer class. Also, the writer instance name is expected to persist between backup and restore, and it is used by VSS to correctly restore multiple-instance writers.

The caller must free the memory held by the <i>pbstrWriterName</i> and <i>pbstrInstanceName</i> parameters by calling <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.

An 
<a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a> interface might be from stored writer state information (created by a call to 
<a href="https://msdn.microsoft.com/cb322541-d8c0-4a2e-9ce5-453d19ac3fd1">CreateVssExamineWriterMetadata</a>). If this is the case, then the following are true:

<ul>
<li><i>pidInstance</i> may not mean anything in terms of live writers.</li>
<li>If <i>pidWriter</i> does not match the writer class of any live writer, a requester should not use that writer's components.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>



<a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a>
 

 

