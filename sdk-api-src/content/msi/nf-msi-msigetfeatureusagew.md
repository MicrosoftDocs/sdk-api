---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# MsiGetFeatureUsageW function


## -description


The 
<b>MsiGetFeatureUsage</b> function returns the usage metrics for a product feature.


## -parameters




### -param szProduct [in]

Specifies the product code for the product that contains the feature.


### -param szFeature [in]

Specifies the feature code for the feature for which metrics are to be returned.


### -param pdwUseCount [out]

Indicates the number of times the feature has been used.


### -param pwDateUsed [out]

Specifies the date that the feature was last used. The date is in the MS-DOS date format, as shown in the following table. 



<table>
<tr>
<th>Bits</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0 – 4</dt>
</dl>
</td>
<td width="60%">
Day of the month (1-31)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>5 – 8</dt>
</dl>
</td>
<td width="60%">
Month (1 = January, 2 = February, and so on)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>9 – 15</dt>
</dl>
</td>
<td width="60%">
Year offset from 1980 (add 1980 to get actual year)

</td>
</tr>
</table>
 


## -returns




					The 
<b>MsiGetFeatureUsage</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_CONFIGURATION</b></dt>
</dl>
</td>
<td width="60%">
The configuration data is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
No usage information is available or the product or feature is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">System Status Functions</a>
 

 

