---
UID: NF:rend.ITDirectoryObjectUser.get_IPPhonePrimary
title: ITDirectoryObjectUser::get_IPPhonePrimary
author: windows-sdk-content
description: The get_IPPhonePrimary method gets the name of a computer that is the primary IP phone for the user.
old-location: tapi3\itdirectoryobjectuser_get_ipphoneprimary.htm
tech.root: tapi
ms.assetid: 43bb9ce5-28ff-4a6f-a55c-a84633e22dfe
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITDirectoryObjectUser interface [TAPI 2.2],get_IPPhonePrimary method, ITDirectoryObjectUser.get_IPPhonePrimary, ITDirectoryObjectUser::get_IPPhonePrimary, _tapi3_itdirectoryobjectuser_get_ipphoneprimary, get_IPPhonePrimary, get_IPPhonePrimary method [TAPI 2.2], get_IPPhonePrimary method [TAPI 2.2],ITDirectoryObjectUser interface, rend/ITDirectoryObjectUser::get_IPPhonePrimary, tapi3.itdirectoryobjectuser_get_ipphoneprimary
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObjectUser.get_IPPhonePrimary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDirectoryObjectUser::get_IPPhonePrimary


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_IPPhonePrimary</b> method gets the name of a computer that is the primary IP phone for the user.


## -parameters




### -param ppName [out]

Pointer to the <b>BSTR</b> representation of the user's IP primary phone.


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
Invalid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/65356507-51d1-479d-8e93-7e18ec041ce3">ITDirectoryObjectUser</a>



<a href="https://msdn.microsoft.com/ba53ea12-7f05-4f68-8a59-915a5906b7be">ITDirectoryObjectUser::put_IPPhonePrimary</a>
 

 

