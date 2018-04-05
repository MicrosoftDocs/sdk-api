---
UID: NF:icm.WcsEnumColorProfilesSize
title: WcsEnumColorProfilesSize function
author: windows-driver-content
description: Returns the size, in bytes, of the buffer that is required by the WcsEnumColorProfiles function to enumerate color profiles.
old-location: wcs\wcsenumcolorprofilessize.htm
old-project: WCS
ms.assetid: 1fc76f8a-dad5-4447-bffc-2df58b4201de
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WcsEnumColorProfilesSize, WcsEnumColorProfilesSize function [Windows Color System], _color_WcsEnumColorProfilesSize, icm/WcsEnumColorProfilesSize, wcs.wcsenumcolorprofilessize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
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
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mscms.dll
api_name:
-	WcsEnumColorProfilesSize
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# WcsEnumColorProfilesSize function


## -description


Returns the size, in bytes, of the buffer that is required by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563720">WcsEnumColorProfiles</a> function to enumerate color profiles.


## -parameters




### -param scope

TBD


### -param pEnumRecord [in]

A pointer to a structure that specifies the enumeration criteria.


### -param pdwSize [out]

A pointer to a variable that receives the size of the buffer that is required to receive all enumerated profile names. This value is used by the <i>dwSize</i> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563720">WcsEnumColorProfiles</a> function.


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff563752">WCS_PROFILE_MANAGEMENT_SCOPE</a> value that specifies the scope of the profile management operation that is performed by this function.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563752">WCS_PROFILE_MANAGEMENT_SCOPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563720">WcsEnumColorProfiles</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

