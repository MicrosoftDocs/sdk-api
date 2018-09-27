---
UID: NF:mfidl.IMFNetCredentialCache.SetGood
title: IMFNetCredentialCache::SetGood
author: windows-sdk-content
description: Reports whether the credential object provided successfully passed the authentication challenge.
old-location: mf\imfnetcredentialcache_setgood.htm
tech.root: medfound
ms.assetid: e2e9d87a-6238-49a0-9a19-fe213749d627
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IMFNetCredentialCache interface [Media Foundation],SetGood method, IMFNetCredentialCache.SetGood, IMFNetCredentialCache::SetGood, SetGood, SetGood method [Media Foundation], SetGood method [Media Foundation],IMFNetCredentialCache interface, e2e9d87a-6238-49a0-9a19-fe213749d627, mf.imfnetcredentialcache_setgood, mfidl/IMFNetCredentialCache::SetGood
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredentialCache.SetGood
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFNetCredentialCache::SetGood


## -description



Reports whether the credential object provided successfully passed the authentication challenge.




## -parameters




### -param pCred [in]

Pointer to the <a href="https://msdn.microsoft.com/d202e7bc-9ce0-4861-8552-5a4d599b1661">IMFNetCredential</a> interface.


### -param fGood [in]

<b>TRUE</b> if the credential object succeeded in the authentication challenge; otherwise, <b>FALSE</b>.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method is called by the network source into the credential manager.




## -see-also




<a href="https://msdn.microsoft.com/d02e26e7-e99c-4be7-8495-830eff2f1554">IMFNetCredentialCache</a>
 

 

