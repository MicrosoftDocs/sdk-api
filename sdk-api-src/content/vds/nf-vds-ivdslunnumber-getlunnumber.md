---
UID: NF:vds.IVdsLunNumber.GetLunNumber
title: IVdsLunNumber::GetLunNumber
author: windows-sdk-content
description: Retrieves the LUN number for a LUN.
old-location: base\ivdslunnumber_getlunnumber.htm
old-project: VDS
ms.assetid: 79aa7dc1-ef46-4b6d-8088-e42839625a16
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLunNumber, GetLunNumber method, GetLunNumber method,IVdsLunNumber interface, IVdsLunNumber interface,GetLunNumber method, IVdsLunNumber.GetLunNumber, IVdsLunNumber::GetLunNumber, base.ivdslunnumber_getlunnumber, vds/IVdsLunNumber::GetLunNumber, vdshwprv/IVdsLunNumber::GetLunNumber
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vds.h
req.include-header: 
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsLunNumber.GetLunNumber
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsLunNumber::GetLunNumber


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Retrieves the LUN number for a LUN.


## -parameters




### -param pulLunNumber [out]

The address of a  variable that receives the LUN number. This value is required and cannot be <b>NULL</b>.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
</table>
 




## -remarks



This method returns the LUN number that the VDS hardware provider assigned to the LUN. This number identifies the LUN  within the disk array.  It is not the same as the "Logical Unit Number" in the disk's SCSI address. Each LUN in the disk array is assigned exactly one LUN number.

This method exists because the DiskRAID utility assigns its own index to each LUN when it enumerates the LUNs in a subsystem. But these indexes can change each time DiskRAID is run, if the hardware provider enumerates the LUNs in a different order. This can be confusing to end users. For disk arrays that have their own (provider-assigned) LUN numbers, this method gives the caller the ability to map the LUN numbers to the LUN indexes that are assigned by DiskRAID.

If a subsystem supports LUN numbering, it can indicate this support by setting the <b>VDS_SF_SUPPORTS_LUN_NUMBER</b> flag in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> or <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> structure. For more information about this flag, see the <a href="https://msdn.microsoft.com/17a07d21-a10a-4f18-a975-def6db073256">VDS_SUB_SYSTEM_FLAG</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/77bd95f7-005a-474f-97c4-e211432b447d">IVdsLunNumber</a>
 

 

