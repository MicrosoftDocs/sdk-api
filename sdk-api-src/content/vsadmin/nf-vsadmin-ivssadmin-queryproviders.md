---
UID: NF:vsadmin.IVssAdmin.QueryProviders
title: IVssAdmin::QueryProviders (vsadmin.h)
author: windows-sdk-content
description: Queries all registered providers.
old-location: base\ivssadmin_queryproviders.htm
tech.root: VSS
ms.assetid: 1267b715-dc2e-47a2-88f1-5c03b5fb5415
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssAdmin interface [VSS],QueryProviders method, IVssAdmin.QueryProviders, IVssAdmin::QueryProviders, QueryProviders, QueryProviders method [VSS], QueryProviders method [VSS],IVssAdmin interface, base.ivssadmin_queryproviders, vsadmin/IVssAdmin::QueryProviders
ms.topic: method
req.header: vsadmin.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsAdmin.h
api_name:
 - IVssAdmin.QueryProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssAdmin::QueryProviders


## -description


The <b>QueryProviders</b> 
   method queries all registered providers.


## -parameters




### -param ppEnum [out]

The address of an <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface pointer, 
      which is initialized on return. Callers must release the interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The query was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The caller is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_UNEXPECTED</b></b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_OBJECT_NOT_FOUND</b></b></dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Expected provider error. The provider logged the error in the event log. For more information, see 
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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Unexpected provider error. The error code is logged in the error log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>
 




## -remarks



Calling the <a href="https://msdn.microsoft.com/9bfaba94-802f-47f5-9843-acc05b32f1b2">IVssEnumObject::Next</a> method on the 
    <a href="https://msdn.microsoft.com/b8e80909-a28a-45d7-87e2-4f44bf6990f4">IVssEnumObject</a> interface returned though the 
    <i>ppEnum</i>  parameter will return 
    <a href="https://msdn.microsoft.com/90664042-e9a0-4959-a975-9289477d2394">VSS_OBJECT_PROP</a> structures containing a 
    <a href="https://msdn.microsoft.com/000da95d-a3f5-447e-a96d-c8fb34e9d0d3">VSS_PROVIDER_PROP</a> structure for each registered 
    provider.




## -see-also




<a href="https://msdn.microsoft.com/6128d627-380b-4fef-b58a-caf8f149f526">IVssAdmin</a>
 

 

