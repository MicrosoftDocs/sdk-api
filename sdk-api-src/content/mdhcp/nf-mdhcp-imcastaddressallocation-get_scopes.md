---
UID: NF:mdhcp.IMcastAddressAllocation.get_Scopes
title: IMcastAddressAllocation::get_Scopes
author: windows-driver-content
description: The get_Scopes method creates a collection of IMcast scopes available. This method is similar to EnumerateScopes, but is used by scripting languages such as Visual Basic.
old-location: tapi3\imcastaddressallocation_get_scopes.htm
old-project: Tapi
ms.assetid: 4fe824fa-2fcb-4f6b-b3de-15dcfc79575c
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMcastAddressAllocation interface [TAPI 2.2],get_Scopes method, IMcastAddressAllocation.get_Scopes, IMcastAddressAllocation::get_Scopes, _tapi3_imcastaddressallocation_get_scopes, get_Scopes, get_Scopes method [TAPI 2.2], get_Scopes method [TAPI 2.2],IMcastAddressAllocation interface, mdhcp/IMcastAddressAllocation::get_Scopes, tapi3.imcastaddressallocation_get_scopes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MODEMSETTINGS, *PMODEMSETTINGS, *LPMODEMSETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mdhcp.dll
api_name:
-	IMcastAddressAllocation.get_Scopes
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMcastAddressAllocation::get_Scopes


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_Scopes</b> method creates a collection of IMcast scopes available. This method is similar to 
<a href="https://msdn.microsoft.com/1845f5f9-be0e-4609-89d8-1a0ed194dd68">EnumerateScopes</a>, but is used by scripting languages such as Visual Basic.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b> receiving an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a> interface pointers.


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
The caller passed in an invalid pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There are no scopes available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to create the required objects.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a> interface returned by <b>IMcastAddressAllocation::get_Scopes</b>. The application must call <b>Release</b> on the 
<b>IMcastScope</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/359e67bb-9a5b-4caa-8d3b-eb0739b0828f">IMcastAddressAllocation</a>



<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

