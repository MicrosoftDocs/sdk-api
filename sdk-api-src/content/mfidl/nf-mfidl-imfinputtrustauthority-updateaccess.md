---
UID: NF:mfidl.IMFInputTrustAuthority.UpdateAccess
title: IMFInputTrustAuthority::UpdateAccess
author: windows-driver-content
description: Notifies the input trust authority (ITA) when the number of output trust authorities (OTAs) that will perform a specified action has changed.
old-location: mf\imfinputtrustauthority_updateaccess.htm
old-project: medfound
ms.assetid: 4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 4ca635fc-15eb-4a9e-8f59-7fa2e3f3e176, IMFInputTrustAuthority interface [Media Foundation],UpdateAccess method, IMFInputTrustAuthority.UpdateAccess, IMFInputTrustAuthority::UpdateAccess, UpdateAccess, UpdateAccess method [Media Foundation], UpdateAccess method [Media Foundation],IMFInputTrustAuthority interface, mf.imfinputtrustauthority_updateaccess, mfidl/IMFInputTrustAuthority::UpdateAccess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFInputTrustAuthority.UpdateAccess
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFInputTrustAuthority::UpdateAccess


## -description



Notifies the input trust authority (ITA) when the number of output trust authorities (OTAs) that will perform a specified action has changed.




## -parameters




### -param pParam [in]

Pointer to an <a href="https://msdn.microsoft.com/5ff3ec3a-a7b1-4378-8e8b-d59a6f5bb28d">MFINPUTTRUSTAUTHORITY_ACCESS_PARAMS</a> structure that contains parameters for the <b>UpdateAccess</b> action.


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



The ITA can update its internal state if needed. If the method returns a failure code, the Media Session cancels the action.




## -see-also




<a href="https://msdn.microsoft.com/637e0225-6fd8-4b83-b4fb-119e7a5ef5d2">IMFInputTrustAuthority</a>
 

 

