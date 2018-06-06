---
UID: NF:ehstorapi.IEnhancedStorageACT.Authorize
title: IEnhancedStorageACT::Authorize
author: windows-sdk-content
description: Associates the Addressable Command Target (ACT) with the Authorized state defined by ACT_AUTHORIZATION_STATE, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT.
old-location: enstor\ienhancedstorageact_authorize.htm
old-project: enstor
ms.assetid: 77141891-9adc-4cd9-b682-8f5b8e842f4c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Authorize, Authorize method [Enhanced Storage], Authorize method [Enhanced Storage],IEnhancedStorageACT interface, IEnhancedStorageACT interface [Enhanced Storage],Authorize method, IEnhancedStorageACT.Authorize, IEnhancedStorageACT::Authorize, ehstorapi/IEnhancedStorageACT::Authorize, enstor.ienhancedstorageact_authorize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TimedLevel
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageACT.Authorize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEnhancedStorageACT::Authorize


## -description


Associates the Addressable Command Target (ACT) with the <b>Authorized</b> state    defined by <a href="https://msdn.microsoft.com/385b2f9d-659e-451d-97da-15be70180e1f">ACT_AUTHORIZATION_STATE</a>, and ensures the authentication of each individual silo according to the required sequence and logical combination necessary to authorize access to the ACT.


## -parameters




### -param hwndParent [in]

Not used.


### -param dwFlags [in]

Not used.


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
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
Authorization completed successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The authorization operation has failed.

</td>
</tr>
</table>
 




## -remarks



This interface method can be used when an application wants to change the ACT to the 'Authorized' state.




## -see-also




<a href="https://msdn.microsoft.com/33d5df30-f877-4852-ad2f-af1bb58d0044">IEnhancedStorageACT</a>
 

 

