---
UID: NF:vswriter.IVssWMDependency.GetWriterId
title: IVssWMDependency::GetWriterId method
author: windows-driver-content
description: The GetWriterId method retrieves the class ID of a writer containing a component that the current component depends on in an explicit writer-component dependency.
old-location: base\ivsswmdependency_getwriterid.htm
old-project: VSS
ms.assetid: 275843c5-3a8c-4add-b453-53ff5d2bb868
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetWriterId method [VSS], GetWriterId method [VSS], IVssWMDependency interface, GetWriterId,IVssWMDependency.GetWriterId, IVssWMDependency, IVssWMDependency interface [VSS], GetWriterId method, IVssWMDependency::GetWriterId, _win32_ivsswmdependency_getwriterid, base.ivsswmdependency_getwriterid, vswriter/IVssWMDependency::GetWriterId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IVssWMDependency.GetWriterId
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWMDependency::GetWriterId method


## -description


The <b>GetWriterId</b> method retrieves the class ID of a writer containing a component that the current component depends on in an explicit writer-component dependency.


## -parameters




### -param pWriterId

The class ID of a writer that manages a component on which the current component depends.


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
Successfully returned the class ID of the writer managing the component that the current component depends on.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No writer can be found that manages the component that the current component depends on.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The pointer <i>pWriterId</i> points to unallocated memory.

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



A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on. A dependency merely indicates that the component and the components it depends on must always be backed up or restored together.

It is possible to have multiple instances of a given writer class; however, any component's logical path and name should be unique.

If there are multiple instances of a writer class, it will be necessary to use logical path and component name information to identify the instance managing the component that the current component depends on.




## -see-also




<a href="https://msdn.microsoft.com/ead9ff63-15dc-4fcc-b341-85ad9c3eabb7">IVssWMComponent::GetDependency</a>



<a href="https://msdn.microsoft.com/5ec3d8d2-5138-4887-9741-addaaaee6bee">IVssWMDependency</a>



<a href="https://msdn.microsoft.com/b0115a42-3c74-41a0-8062-0f20123780fe">IVssWMDependency::GetComponentName</a>



<a href="https://msdn.microsoft.com/642e9266-40b8-4184-b83f-3131886da32b">IVssWMDependency::GetLogicalPath</a>
 

 

