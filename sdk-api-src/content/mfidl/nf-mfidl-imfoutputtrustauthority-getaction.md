---
UID: NF:mfidl.IMFOutputTrustAuthority.GetAction
title: IMFOutputTrustAuthority::GetAction
author: windows-sdk-content
description: Retrieves the action that is performed by this output trust authority (OTA).
old-location: mf\imfoutputtrustauthority_getaction.htm
tech.root: medfound
ms.assetid: 5a109e18-a6e2-4f8c-a656-b27112935452
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5a109e18-a6e2-4f8c-a656-b27112935452, GetAction, GetAction method [Media Foundation], GetAction method [Media Foundation],IMFOutputTrustAuthority interface, IMFOutputTrustAuthority interface [Media Foundation],GetAction method, IMFOutputTrustAuthority.GetAction, IMFOutputTrustAuthority::GetAction, mf.imfoutputtrustauthority_getaction, mfidl/IMFOutputTrustAuthority::GetAction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFOutputTrustAuthority.GetAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFOutputTrustAuthority::GetAction


## -description



Retrieves the action that is performed by this output trust authority (OTA).




## -parameters




### -param pAction [out]

Receives a member of the <a href="https://msdn.microsoft.com/74cee983-e084-458b-b615-5447cca9abbc">MFPOLICYMANAGER_ACTION</a> enumeration.


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
 




## -see-also




<a href="https://msdn.microsoft.com/21594ac0-7e3c-44a3-bbee-64316dd51824">IMFOutputTrustAuthority</a>
 

 

