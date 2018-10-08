---
UID: NF:icm.WcsEnumColorProfiles
title: WcsEnumColorProfiles function
author: windows-sdk-content
description: Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.
old-location: wcs\wcsenumcolorprofiles.htm
tech.root: WCS
ms.assetid: 45d670ae-a2f1-4281-bcd8-0663ee3e7fe4
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: WcsEnumColorProfiles, WcsEnumColorProfiles function [Windows Color System], WcsEnumColorProfilesA, WcsEnumColorProfilesW, _color_WcsEnumColorProfiles, icm/WcsEnumColorProfiles, icm/WcsEnumColorProfilesA, icm/WcsEnumColorProfilesW, wcs.wcsenumcolorprofiles
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
req.unicode-ansi: WcsEnumColorProfilesW (Unicode) and WcsEnumColorProfilesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - WcsEnumColorProfiles
 - WcsEnumColorProfilesA
 - WcsEnumColorProfilesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcsEnumColorProfiles function


## -description


Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.


## -parameters




### -param scope

TBD


### -param pEnumRecord [in]

A pointer to a structure specifying the enumeration criteria.


### -param pBuffer [out]

A pointer to a buffer in which the profile names are to be enumerated. The <b>WcsEnumColorProfiles</b> function places, in this buffer, a MULTI_SZ string that consists of profile names that satisfy the criteria specified in <i>*pEnumRecord</i>.


### -param dwSize [in]

A variable that contains the size, in bytes, of the buffer that is pointed to by <i>pBuffer</i>. See Remarks.


### -param pnProfiles [out, optional]

An optional pointer to a variable that receives the number of profile names that are copied to the buffer to which <i>pBuffer</i> points. Can be <b>NULL</b> if this information is not needed.


#### - profileManagementScope [in]

A <a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a> value specifying the scope of this profile management operation.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



Use the <a href="https://msdn.microsoft.com/1fc76f8a-dad5-4447-bffc-2df58b4201de">WcsEnumColorProfilesSize</a> function to retrieve the value for the <i>dwSize</i> parameter, which is the size, in bytes, of the buffer pointed to by the <i>pBuffer</i> parameter.

If the <i>profileManagementScope</i> parameter is WCS_PROFILE_MANAGEMENT_SCOPE_SYSTEM_WIDE, only system-wide associations of profiles to the device are considered. If <i>profileManagementScope</i> is WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER, only per-user associations for the current user are considered. If <a href="https://msdn.microsoft.com/c108fbb2-e9f3-41fe-af36-99114df1507e">WcsSetUsePerUserProfiles</a> has never been called for this user, or if <b>WcsSetUsePerUserProfiles</b> was most recently called for this user with its <i>usePerUserProfiles</i> parameter set to <b>FALSE</b>, then <b>WCSEnumColorProfiles</b> returns an empty list.

If WCS_PROFILE_MANAGEMENT_SCOPE_CURRENT_USER (the current user setting) is present, it overrides the system-wide default for the <i>profileManagementScope</i> parameter.

This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/6895a807-81da-4263-b370-977ecfaffac8">WCS_PROFILE_MANAGEMENT_SCOPE</a>



<a href="https://msdn.microsoft.com/1fc76f8a-dad5-4447-bffc-2df58b4201de">WcsEnumColorProfilesSize</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

