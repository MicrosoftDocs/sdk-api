---
UID: NF:vds.IVdsServiceIscsi.GetInitiatorName
title: IVdsServiceIscsi::GetInitiatorName (vds.h)
author: windows-sdk-content
description: Returns the iSCSI name of the local initiator service.
old-location: base\ivdsserviceiscsi_getinitiatorname.htm
tech.root: VDS
ms.assetid: 34f18293-6254-4f73-a633-642a3cdeaf31
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInitiatorName, GetInitiatorName method [VDS], GetInitiatorName method [VDS],IVdsServiceIscsi interface, IVdsServiceIscsi interface [VDS],GetInitiatorName method, IVdsServiceIscsi.GetInitiatorName, IVdsServiceIscsi::GetInitiatorName, base.ivdsserviceiscsi_getinitiatorname, vds/IVdsServiceIscsi::GetInitiatorName
ms.topic: method
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsServiceIscsi.GetInitiatorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
---

# IVdsServiceIscsi::GetInitiatorName


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the iSCSI name of the local initiator service.


## -parameters




### -param ppwszIscsiName [out]

The address of a pointer to a string. VDS will put a pointer to an initialized string at this location. 
      Callers must free the string by using the 
      <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

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
The name was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppwszIscsiName</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/07bbfb4b-f054-4ec2-8f0b-3910115db5c1">IVdsServiceIscsi</a>
 

 

