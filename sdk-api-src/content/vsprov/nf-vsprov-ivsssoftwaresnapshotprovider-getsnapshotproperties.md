---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.GetSnapshotProperties
title: IVssSoftwareSnapshotProvider::GetSnapshotProperties
author: windows-driver-content
description: Gets the properties of the specified shadow copy.
old-location: base\ivsssoftwaresnapshotprovider_getsnapshotproperties.htm
old-project: VSS
ms.assetid: 59886344-d594-4eb8-9718-ab11a6627e8e
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetSnapshotProperties, GetSnapshotProperties method, GetSnapshotProperties method,IVssSoftwareSnapshotProvider interface, IVssSoftwareSnapshotProvider interface,GetSnapshotProperties method, IVssSoftwareSnapshotProvider.GetSnapshotProperties, IVssSoftwareSnapshotProvider::GetSnapshotProperties, base.ivsssoftwaresnapshotprovider_getsnapshotproperties, vsprov/IVssSoftwareSnapshotProvider::GetSnapshotProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsprov.h
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
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssSoftwareSnapshotProvider.GetSnapshotProperties
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssSoftwareSnapshotProvider::GetSnapshotProperties


## -description


Gets the properties of the specified shadow copy.


## -parameters




### -param SnapshotId [in]

Shadow copy identifier.


### -param pProp [out]

The address of a caller-allocated <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure that receives the shadow copy properties. The provider is responsible for setting the members of this structure. All members are required except  <b>m_pwszExposedName</b> and <b>m_pwszExposedPath</b>, which the provider can set to <b>NULL</b>. The provider allocates memory for all string members  that it sets in the structure. When the structure is no longer needed, the caller is responsible for freeing these strings by calling the <a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a> function.


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
The requested information was successfully returned.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified volume was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">

        Provider error. The provider logged the error in the event log. For more information, see 
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



The caller should set the contents of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure to zero before calling the <b>GetSnapshotProperties</b> method.

The provider is responsible for allocating and freeing the strings in the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/5c95f2fb-c132-489c-af48-2ffafad0b41f">IVssSoftwareSnapshotProvider</a>



<a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a>
 

 

