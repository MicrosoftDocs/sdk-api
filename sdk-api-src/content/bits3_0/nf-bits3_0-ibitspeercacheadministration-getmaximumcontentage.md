---
UID: NF:bits3_0.IBitsPeerCacheAdministration.GetMaximumContentAge
title: IBitsPeerCacheAdministration::GetMaximumContentAge
author: windows-driver-content
description: Gets the age by when files are removed from the cache.
old-location: bits\ibitspeercacheadministration_getmaximumcontentage.htm
old-project: Bits
ms.assetid: 6b6b0c97-9906-464d-b267-5adde1919a45
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: GetMaximumContentAge, GetMaximumContentAge method [BITS], GetMaximumContentAge method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],GetMaximumContentAge method, IBitsPeerCacheAdministration.GetMaximumContentAge, IBitsPeerCacheAdministration::GetMaximumContentAge, bits.ibitspeercacheadministration_getmaximumcontentage, bits3_0/IBitsPeerCacheAdministration::GetMaximumContentAge
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bits.lib
-	Bits.dll
api_name:
-	IBitsPeerCacheAdministration.GetMaximumContentAge
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheAdministration::GetMaximumContentAge


## -description


Gets the age by when files are removed from the cache.


## -parameters




### -param pSeconds [out]

Age, in seconds. If the last time that the file was accessed is older than this age, BITS removes the file from the cache. 


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/815d9e48-f1f0-4c40-a277-d78db9d6ace1">IBitsPeerCacheAdministration::SetMaximumContentAge</a>
 

 

