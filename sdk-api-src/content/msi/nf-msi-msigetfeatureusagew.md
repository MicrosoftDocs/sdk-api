---
UID: NF:msi.MsiGetFeatureUsageW
title: MsiGetFeatureUsageW function
author: windows-driver-content
description: The MsiGetFeatureUsage function returns the usage metrics for a product feature.
old-location: setup\msigetfeatureusage.htm
old-project: Msi
ms.assetid: ab347f39-e1f6-4cb2-85ff-bad872b5256f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MsiGetFeatureUsage, MsiGetFeatureUsage function, MsiGetFeatureUsageA, MsiGetFeatureUsageW, _msi_msigetfeatureusage, msi/MsiGetFeatureUsage, msi/MsiGetFeatureUsageA, msi/MsiGetFeatureUsageW, setup.msigetfeatureusage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiGetFeatureUsageW (Unicode) and MsiGetFeatureUsageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DRM_CLIENT_VERSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msi.dll
api_name:
-	MsiGetFeatureUsage
-	MsiGetFeatureUsageA
-	MsiGetFeatureUsageW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

