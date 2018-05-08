---
UID: NF:mfidl.IMFOutputPolicy.GetMinimumGRLVersion
title: IMFOutputPolicy::GetMinimumGRLVersion
author: windows-driver-content
description: Retrieves the minimum version of the global revocation list (GRL) that must be enforced by the protected environment for this policy.
old-location: mf\imfoutputpolicy_getminimumgrlversion.htm
old-project: medfound
ms.assetid: 41da430b-9cdd-4ab0-873d-f6d94f48d401
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 41da430b-9cdd-4ab0-873d-f6d94f48d401, GetMinimumGRLVersion, GetMinimumGRLVersion method [Media Foundation], GetMinimumGRLVersion method [Media Foundation],IMFOutputPolicy interface, IMFOutputPolicy interface [Media Foundation],GetMinimumGRLVersion method, IMFOutputPolicy.GetMinimumGRLVersion, IMFOutputPolicy::GetMinimumGRLVersion, mf.imfoutputpolicy_getminimumgrlversion, mfidl/IMFOutputPolicy::GetMinimumGRLVersion
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
-	IMFOutputPolicy.GetMinimumGRLVersion
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFOutputPolicy::GetMinimumGRLVersion


## -description



Retrieves the minimum version of the global revocation list (GRL) that must be enforced by the protected environment for this policy.




## -parameters




### -param pdwMinimumGRLVersion [out]

Receives the minimum GRL version.


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




<a href="https://msdn.microsoft.com/76af8e03-9584-4f4b-ab2c-8a0ff2c3485b">IMFOutputPolicy</a>
 

 

