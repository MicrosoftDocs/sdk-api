---
UID: NF:rend.ITDirectory.get_DisplayName
title: ITDirectory::get_DisplayName
author: windows-sdk-content
description: The get_DisplayName method gets displayable name for directory.
old-location: tapi3\itdirectory_get_displayname.htm
old-project: Tapi
ms.assetid: a564e501-089e-41fc-9e81-bd0c9e6f951d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_DisplayName method, ITDirectory.get_DisplayName, ITDirectory::get_DisplayName, _tapi3_itdirectory_get_displayname, get_DisplayName, get_DisplayName method [TAPI 2.2], get_DisplayName method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_DisplayName, tapi3.itdirectory_get_displayname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectory.get_DisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITDirectory::get_DisplayName


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DisplayName</b> method gets displayable name for directory.


## -parameters




### -param pName [out]

Pointer to a <b>BSTR</b> representation of the directory name.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pName</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not yet implemented.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>pName</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>
 

 

