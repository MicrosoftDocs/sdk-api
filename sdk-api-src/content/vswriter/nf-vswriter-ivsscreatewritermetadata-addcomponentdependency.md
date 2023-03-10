---
UID: NF:vswriter.IVssCreateWriterMetadata.AddComponentDependency
title: IVssCreateWriterMetadata::AddComponentDependency (vswriter.h)
description: The AddComponentDependency method allows a writer to indicate that a component it manages has an explicit writer-component dependency; that is, another component in another writer must be backed up and restored with it.
helpviewer_keywords: ["AddComponentDependency","AddComponentDependency method [VSS]","AddComponentDependency method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddComponentDependency method","IVssCreateWriterMetadata.AddComponentDependency","IVssCreateWriterMetadata::AddComponentDependency","_win32_ivsscreatewritermetadata_addcomponentdependency","base.ivsscreatewritermetadata_addcomponentdependency","vswriter/IVssCreateWriterMetadata::AddComponentDependency"]
old-location: base\ivsscreatewritermetadata_addcomponentdependency.htm
tech.root: base
ms.assetid: cc6c8ab6-3706-4c75-ba31-cc8c1dc4dd06
ms.date: 12/05/2018
ms.keywords: AddComponentDependency, AddComponentDependency method [VSS], AddComponentDependency method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddComponentDependency method, IVssCreateWriterMetadata.AddComponentDependency, IVssCreateWriterMetadata::AddComponentDependency, _win32_ivsscreatewritermetadata_addcomponentdependency, base.ivsscreatewritermetadata_addcomponentdependency, vswriter/IVssCreateWriterMetadata::AddComponentDependency
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssCreateWriterMetadata::AddComponentDependency
 - vswriter/IVssCreateWriterMetadata::AddComponentDependency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateWriterMetadata.AddComponentDependency
---

# IVssCreateWriterMetadata::AddComponentDependency


## -description

The 
<b>AddComponentDependency</b> method allows a writer to indicate that a component it manages has an explicit writer-component dependency; that is, another component in another writer must be backed up and restored with it.

## -parameters

### -param wszForLogicalPath [in]

A null-terminated wide character string containing the logical path of the component (managed by the current writer) that requires a dependency.

### -param wszForComponentName [in]

A null-terminated wide character string containing the component (managed by the current writer) that requires a dependency.

### -param onWriterId [in]

The class ID or 
<a href="/windows/desktop/VSS/volume-shadow-copy-api-data-types">VSS_ID</a> (GUID) of the writer managing the component on which the current component depends.

### -param wszOnLogicalPath [in]

The logical path of the component (managed by the writer identified by <i>onWriterId</i>) on which the current component depends.

### -param wszOnComponentName [in]

The name of the component (managed by the writer identified by <i>onWriterId</i>) on which the current component depends.

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
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

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
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

Dependencies upon components managed by the current writer are not permitted.

A dependency requires that both the target of the dependency and the component that depends on the target be restored and backed up together. It does not indicate a priority between the components, although a requester may choose to implement that.

Because the combination of logical name and component name must be unique across all instances of a writer class, the fact that several writers may have the same class ID is not a problem.

This method can be used to declare remote dependencies. A writer can declare a remote dependency by prepending "&#92;&#92;<i>RemoteComputerName</i>\", where <i>RemoteComputerName</i> is the name of the computer where the remote component resides, to the logical path in the <i>wszOnLogicalPath</i> parameter. The value of <i>RemoteComputerName</i> can be an IP address or a computer name returned by the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a> function.

If the remote component resides on a cluster, the writer must report the virtual name for the cluster, and it is the requester's responsibility to map the virtual name to the physical name of a cluster node before a volume shadow copy can be created.

To determine whether a dependency is local or remote, the requester must examine the component name returned in the <i>pbstrComponentName</i> parameter. If the component name begins with "\\", the requester must assume that it specifies a remote dependency and that the first component following "\\" is the <i>RemoteComputerName</i> that was specified by the writer. If the component name does not begin with "\\", the requester should assume that it specifies a local dependency.

<b>Windows Server 2003:  </b>This method cannot be used to declare remote dependencies until Windows Server 2003 with Service Pack 1 (SP1).