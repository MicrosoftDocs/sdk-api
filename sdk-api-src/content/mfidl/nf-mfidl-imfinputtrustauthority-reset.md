---
UID: NF:mfidl.IMFInputTrustAuthority.Reset
title: IMFInputTrustAuthority::Reset
author: windows-sdk-content
description: Resets the input trust authority (ITA) to its initial state.
old-location: mf\imfinputtrustauthority_reset.htm
old-project: medfound
ms.assetid: beb8e598-5a35-46b0-aa13-6bef38b9defb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFInputTrustAuthority interface [Media Foundation],Reset method, IMFInputTrustAuthority.Reset, IMFInputTrustAuthority::Reset, Reset, Reset method [Media Foundation], Reset method [Media Foundation],IMFInputTrustAuthority interface, beb8e598-5a35-46b0-aa13-6bef38b9defb, mf.imfinputtrustauthority_reset, mfidl/IMFInputTrustAuthority::Reset
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFInputTrustAuthority.Reset
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFInputTrustAuthority::Reset


## -description



Resets the input trust authority (ITA) to its initial state.




## -parameters






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



When this method is called, the ITA should disable any decrypter that was returned in the <a href="https://msdn.microsoft.com/3bc4e2e6-41a8-4751-a7fe-5e1f8c136983">IMFInputTrustAuthority::GetDecrypter</a> method.




## -see-also




<a href="https://msdn.microsoft.com/637e0225-6fd8-4b83-b4fb-119e7a5ef5d2">IMFInputTrustAuthority</a>
 

 

