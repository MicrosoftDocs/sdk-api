---
UID: NF:vsbackup.IVssWMComponent.GetDependency
title: IVssWMComponent::GetDependency
author: windows-sdk-content
description: The GetDependency method returns an instance of the IVssWMDependency interface containing accessors for obtaining information about explicit writer-component dependencies of one of the current components.
old-location: base\ivsswmcomponent_getdependency.htm
tech.root: VSS
ms.assetid: ead9ff63-15dc-4fcc-b341-85ad9c3eabb7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDependency, GetDependency method [VSS], GetDependency method [VSS],IVssWMComponent interface, IVssWMComponent interface [VSS],GetDependency method, IVssWMComponent.GetDependency, IVssWMComponent::GetDependency, _win32_ivsswmcomponent_getdependency, base.ivsswmcomponent_getdependency, vsbackup/IVssWMComponent::GetDependency
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssWMComponent.GetDependency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssWMComponent::GetDependency


## -description


The 
<b>GetDependency</b> method returns an instance of the 
<a href="https://msdn.microsoft.com/5ec3d8d2-5138-4887-9741-addaaaee6bee">IVssWMDependency</a> interface containing accessors for obtaining information about explicit writer-component dependencies of one of the current components.


## -parameters




### -param iDependency [in]

Offset between 0 and <i>n</i>-1, where <i>n</i> is the number of dependencies associated with this component as specified by the <b>cDependencies</b> member of the 
<a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a> object returned by 
<a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">IVssWMComponent::GetComponentInfo</a>.


### -param ppDependency [out]

Doubly indirect pointer to an instance of the 
<a href="https://msdn.microsoft.com/5ec3d8d2-5138-4887-9741-addaaaee6bee">IVssWMDependency</a> interface.


## -returns



This method can return one of these values.

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
The component specified by the index <i>iDependency</i> does not exist.

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



The caller is responsible for calling <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> to release system resources held by the returned 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object.




## -see-also




<a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a>



<a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">IVssWMComponent::GetComponentInfo</a>



<a href="https://msdn.microsoft.com/5ec3d8d2-5138-4887-9741-addaaaee6bee">IVssWMDependency</a>



<a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a>
 

 

