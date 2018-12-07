---
UID: NF:bits3_0.IBitsPeerCacheAdministration.SetMaximumContentAge
title: IBitsPeerCacheAdministration::SetMaximumContentAge
author: windows-sdk-content
description: Specifies when files are removed from the cache based on age.
old-location: bits\ibitspeercacheadministration_setmaximumcontentage.htm
tech.root: bits
ms.assetid: 815d9e48-f1f0-4c40-a277-d78db9d6ace1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBitsPeerCacheAdministration interface [BITS],SetMaximumContentAge method, IBitsPeerCacheAdministration.SetMaximumContentAge, IBitsPeerCacheAdministration::SetMaximumContentAge, SetMaximumContentAge, SetMaximumContentAge method [BITS], SetMaximumContentAge method [BITS],IBitsPeerCacheAdministration interface, bits.ibitspeercacheadministration_setmaximumcontentage, bits3_0/IBitsPeerCacheAdministration::SetMaximumContentAge
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
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration.SetMaximumContentAge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration::SetMaximumContentAge


## -description


Specifies when files are removed from the cache based on age.


## -parameters




### -param Seconds [in]

Age, in seconds. If the last time that the file was accessed is older than this age, BITS removes the file from the cache. The age is reset each time the file is accessed. The maximum value is 10,368,000 seconds (120 days) and the minimum value is 86,400 seconds (1 day). The default is 7,776,000 seconds (90 days).


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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.

</td>
</tr>
</table>
 




## -remarks



This value is used only if the MaxContentAge group policy is not set.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964286(v=VS.85).aspx">IBitsPeerCacheAdministration::GetMaximumContentAge</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964289(v=VS.85).aspx">IBitsPeerCacheAdministration::SetMaximumCacheSize</a>
 

 

