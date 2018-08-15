---
UID: NF:instance.CInstance.GetWCHAR
title: CInstance::GetWCHAR
author: windows-sdk-content
description: The GetWCHAR method retrieves a WCHAR string property.
old-location: wmi\cinstance_getwchar.htm
old-project: WmiSdk
ms.assetid: 1c2f3dfc-aa84-4dff-a25b-b8f2ec3afa74
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CInstance interface [Windows Management Instrumentation],GetWCHAR method, CInstance.GetWCHAR, CInstance::GetWCHAR, GetWCHAR, GetWCHAR method [Windows Management Instrumentation], GetWCHAR method [Windows Management Instrumentation],CInstance interface, _hmm_cinstance_getwchar, instance/CInstance::GetWCHAR, wmi.cinstance_getwchar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: instance.h
req.include-header: FwCommon.h
req.redist: 
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
tech.root: 
req.typenames: TrustLevel
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CInstance.GetWCHAR
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
req.product: GDI+ 1.1
---

# CInstance::GetWCHAR


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetWCHAR</b> method retrieves a <b>WCHAR</b> string property.


## -parameters




### -param name

Name of the <b>WCHAR</b> string property retrieved.


### -param pW






#### - pw

Buffer that receives the <b>WCHAR</b> string property.


## -returns



Returns <b>TRUE</b> if the operation was successful and <b>FALSE</b> if an attempt was made to retrieve a property that is not a type that is <b>WCHAR</b> string-compatible or a property that does not exist. More information is available in the log file, Framework.log.




## -remarks



It is the responsibility of the implementer to free the memory occupied by the <b>WCHAR</b> string:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    free(pw);</pre>
</td>
</tr>
</table></span></div>
Use <b>free</b> rather than <b>delete</b> because the provider framework allocates the string using <b>malloc</b> and does not use the <b>new</b> operator.



