---
UID: NF:rend.ITDirectoryObjectUser.put_IPPhonePrimary
title: ITDirectoryObjectUser::put_IPPhonePrimary
author: windows-sdk-content
description: The put_IPPhonePrimary method sets the name of a machine as the primary IP phone for a user.
old-location: tapi3\itdirectoryobjectuser_put_ipphoneprimary.htm
old-project: tapi
ms.assetid: ba53ea12-7f05-4f68-8a59-915a5906b7be
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITDirectoryObjectUser interface [TAPI 2.2],put_IPPhonePrimary method, ITDirectoryObjectUser.put_IPPhonePrimary, ITDirectoryObjectUser::put_IPPhonePrimary, _tapi3_itdirectoryobjectuser_put_ipphoneprimary, put_IPPhonePrimary, put_IPPhonePrimary method [TAPI 2.2], put_IPPhonePrimary method [TAPI 2.2],ITDirectoryObjectUser interface, rend/ITDirectoryObjectUser::put_IPPhonePrimary, tapi3.itdirectoryobjectuser_put_ipphoneprimary
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
 - ITDirectoryObjectUser.put_IPPhonePrimary
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITDirectoryObjectUser::put_IPPhonePrimary


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_IPPhonePrimary</b> method sets the name of a machine as the primary IP phone for a user.


## -parameters




### -param pName [in]

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



This method can be used only on a new object that is subsequently added to the directory. If an application wants to modify the IP phone of an existing user object, it has to enumerate the objects from the server to determine the old IP phones are. This implies that a TAPI 3 application is running on one or more other machines. The application on a local machine has no information about whether those other applications are still running. Therefore, it is not the application's place to change the IP Phone on existing user objects.

To modify an existing user's IP Phone, the user must be deleted and re-added.

The application must use 
<a href="https://msdn.microsoft.com/library/ms221458(v=VS.85).aspx">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory when the variable is no longer needed.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/65356507-51d1-479d-8e93-7e18ec041ce3">ITDirectoryObjectUser</a>



<a href="https://msdn.microsoft.com/43bb9ce5-28ff-4a6f-a55c-a84633e22dfe">ITDirectoryObjectUser::get_IPPhonePrimary</a>
 

 

