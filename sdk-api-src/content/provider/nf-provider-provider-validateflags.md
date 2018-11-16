---
UID: NF:provider.Provider.ValidateFlags
title: Provider::ValidateFlags
author: windows-sdk-content
description: The ValidateFlags method determines whether a set of flags is valid.
old-location: wmi\provider_validateflags.htm
tech.root: WmiSdk
ms.assetid: 1d6d1006-99b9-4646-a5c4-835940ce3ac0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Provider interface [Windows Management Instrumentation],ValidateFlags method, Provider.ValidateFlags, Provider::ValidateFlags, ValidateFlags, ValidateFlags method [Windows Management Instrumentation], ValidateFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validateflags, provider/Provider::ValidateFlags, wmi.provider_validateflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: provider.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.ValidateFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- provider.h
: 
- Provider.ValidateFlags
: 
---

# Provider::ValidateFlags


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/d8a7c433-7e6a-45cc-914f-a15a3688c7aa">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>ValidateFlags</b> method determines whether a set of flags is valid.


## -parameters




### -param lFlags

Bitmask of flags that are validated.


### -param lAcceptableFlags

Bitmask of <i>IFlags</i> values that are acceptable to the calling method. For more information, see Remarks.


## -returns



Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.




## -remarks



This helper method can be called by an override of any of the following virtual methods to indicate which flags are acceptable as arguments to the virtual method:

<ul>
<li>
<a href="https://msdn.microsoft.com/eaaf49e3-e768-4494-ba0b-dc2c8c35be47">Provider::ValidateDeletionFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1f5ae240-2314-40c1-a6c8-2c395d284568">Provider::ValidateEnumerationFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5090c47b-062b-4359-b03b-0d05c225447d">Provider::ValidateGetObjFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/febc48d8-8952-4e2f-80fc-40344908f8b2">Provider::ValidateMethodFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dd7a480e-9569-45ed-a46d-218c1a9cf2db">Provider::ValidatePutInstanceFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b35e6f2f-7d40-4b9b-833d-63efafd06a20">Provider::ValidateQueryFlags</a>
</li>
</ul>
The values for <i>IAcceptableFlags</i> are limited to the <a href="https://msdn.microsoft.com/B5F1F8DD-9769-40A6-B743-4F4DF4B8C363">FlagDefs</a> enumeration defined as the following:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    enum FlagDefs
    {
        EnumerationFlags = 0,
        GetObjFlags = 0,
        MethodFlags = 0,
        DeletionFlags = 0,
        PutInstanceFlags = (WBEM_FLAG_CREATE_OR_UPDATE |
                            WBEM_FLAG_CREATE_ONLY |
                            WBEM_FLAG_UPDATE_ONLY),
        QueryFlags = 0
    };</pre>
</td>
</tr>
</table></span></div>


