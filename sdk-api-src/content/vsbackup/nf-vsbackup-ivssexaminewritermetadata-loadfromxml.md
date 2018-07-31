---
UID: NF:vsbackup.IVssExamineWriterMetadata.LoadFromXML
title: IVssExamineWriterMetadata::LoadFromXML
author: windows-sdk-content
description: The LoadFromXML method loads an XML document that contains a writer's metadata document into an IVssExamineWriterMetadata interface.
old-location: base\ivssexaminewritermetadata_loadfromxml.htm
old-project: VSS
ms.assetid: 8a508a2c-1c42-4414-9c54-a78d1e1564a0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVssExamineWriterMetadata interface [VSS],LoadFromXML method, IVssExamineWriterMetadata.LoadFromXML, IVssExamineWriterMetadata::LoadFromXML, LoadFromXML, LoadFromXML method [VSS], LoadFromXML method [VSS],IVssExamineWriterMetadata interface, _win32_ivssexaminewritermetadata_loadfromxml, base.ivssexaminewritermetadata_loadfromxml, vsbackup/IVssExamineWriterMetadata::LoadFromXML
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssExamineWriterMetadata.LoadFromXML
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExamineWriterMetadata::LoadFromXML


## -description


The 
<b>LoadFromXML</b> method loads an XML document that contains a writer's metadata document into an 
<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface.


## -parameters




### -param bstrXML [in]

String that contains an XML document that represents a writer's metadata document.


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
Successfully added the <i>bstrXML</i> parameter value to the XML document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The XML document could not be loaded.

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
The XML document is not valid. Check the event log for details. For more information, see 
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



This method is used at restore time to load writer metadata that was saved by 
<a href="https://msdn.microsoft.com/146dcd00-e479-40fa-963b-e7111b783822">IVssExamineWriterMetadata::SaveAsXML</a> at the time of the backup operation.

Users should not tamper with this metadata document.




## -see-also




<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/146dcd00-e479-40fa-963b-e7111b783822">IVssExamineWriterMetadata::SaveAsXML</a>
 

 

