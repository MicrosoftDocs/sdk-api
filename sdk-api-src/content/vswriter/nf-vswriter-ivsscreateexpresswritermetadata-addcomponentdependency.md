---
UID: NF:vswriter.IVssCreateExpressWriterMetadata.AddComponentDependency
title: IVssCreateExpressWriterMetadata::AddComponentDependency
author: windows-sdk-content
description: Allows an express writer to indicate that a component it manages has an explicit writer-component dependency; that is, another component (possibly managed by another writer) must be backed up and restored with it.
old-location: base\ivsscreateexpresswritermetadata_addcomponentdependency.htm
old-project: vss
ms.assetid: 1d7e28de-8bb7-4ab4-bcdd-554d47007233
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddComponentDependency, AddComponentDependency method, AddComponentDependency method,IVssCreateExpressWriterMetadata interface, IVssCreateExpressWriterMetadata interface,AddComponentDependency method, IVssCreateExpressWriterMetadata.AddComponentDependency, IVssCreateExpressWriterMetadata::AddComponentDependency, base.ivsscreateexpresswritermetadata_addcomponentdependency, vswriter/IVssCreateExpressWriterMetadata::AddComponentDependency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateExpressWriterMetadata.AddComponentDependency
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssCreateExpressWriterMetadata::AddComponentDependency


## -description


Allows an express writer to indicate that a component it manages has an explicit writer-component dependency; that is, another component (possibly managed by another writer) must be backed up and restored with it.


## -parameters




### -param wszForLogicalPath [in]

A null-terminated wide character string containing the logical path of the component (managed by the express writer) that requires a dependency.


### -param wszForComponentName [in]

A null-terminated wide character string containing the component (managed by the express writer) that requires a dependency.


### -param onWriterId [in]

A 
<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a> (GUID) value that specifies the writer class of the express writer managing the component on which the current component depends.


### -param wszOnLogicalPath [in]

The logical path of the component (managed by the express writer identified by <i>onWriterId</i>) on which the current component depends.


### -param wszOnComponentName [in]

The name of the component (managed by the express writer identified by <i>onWriterId</i>) on which the current component depends.


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
The operation was successful.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The component specified by <i>wszForLogicalPath</i> and <i>wszForComponentName</i> does not exist.

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
 




## -see-also




<a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a>
 

 

