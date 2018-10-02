---
UID: NF:bits3_0.IBitsPeerCacheAdministration.SetMaximumCacheSize
title: IBitsPeerCacheAdministration::SetMaximumCacheSize
author: windows-sdk-content
description: Specifies the maximum size of the cache.
old-location: bits\ibitspeercacheadministration_setmaximumcachesize.htm
tech.root: Bits
ms.assetid: 064376cf-8865-45a1-a63a-1096bc0d58ce
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBitsPeerCacheAdministration interface [BITS],SetMaximumCacheSize method, IBitsPeerCacheAdministration.SetMaximumCacheSize, IBitsPeerCacheAdministration::SetMaximumCacheSize, SetMaximumCacheSize, SetMaximumCacheSize method [BITS], SetMaximumCacheSize method [BITS],IBitsPeerCacheAdministration interface, bits.ibitspeercacheadministration_setmaximumcachesize, bits3_0/IBitsPeerCacheAdministration::SetMaximumCacheSize
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
 - IBitsPeerCacheAdministration.SetMaximumCacheSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheAdministration::SetMaximumCacheSize


## -description


Specifies the maximum size of the cache.


## -parameters




### -param Bytes [in]

Maximum size of the cache, as a percentage of available hard disk drive space.


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



This value is used only if the MaxCacheSize group policy is not set.

If the maximum cache size is reached, BITS removes the least recently accessed files until the necessary disk space is freed. If you specify a value that is less than the current cache size, BITS removes files from the cache until the requested size is met. BITS removes the files based on <a href="https://msdn.microsoft.com/en-us/library/Aa964290(v=VS.85).aspx">age</a>. Files that are larger than the cache size are not cached.

By default, the maximum cache size is 1% of the disk size.    BITS does not use the limit to reserve disk space for the cache. BITS will use up to the specified limit for the cache, if the disk space is available. The maximum value you can specify is 80% of the disk size.

If the request is to reduce the size of the cache and BITS is currently downloading a file from the cache, BITS will not remove the file until the download is complete.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa964272(v=VS.85).aspx">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964282(v=VS.85).aspx">IBitsPeerCacheAdministration::GetMaximumCacheSize</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa964290(v=VS.85).aspx">IBitsPeerCacheAdministration::SetMaximumContentAge</a>
 

 

