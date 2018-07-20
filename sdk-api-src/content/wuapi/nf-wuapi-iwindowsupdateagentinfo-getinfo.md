---
UID: NF:wuapi.IWindowsUpdateAgentInfo.GetInfo
title: IWindowsUpdateAgentInfo::GetInfo
author: windows-sdk-content
description: Retrieves version information about Windows Update Agent (WUA).
old-location: wua\iwindowsupdateagentinfo_getinfo.htm
old-project: Wua_Sdk
ms.assetid: 7798032c-b0a3-4f2a-958a-f98192204832
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetInfo, GetInfo method [Windows Update Agent], GetInfo method [Windows Update Agent],IWindowsUpdateAgentInfo interface, IWindowsUpdateAgentInfo interface [Windows Update Agent],GetInfo method, IWindowsUpdateAgentInfo.GetInfo, IWindowsUpdateAgentInfo::GetInfo, wua.iwindowsupdateagentinfo_getinfo, wuapi/IWindowsUpdateAgentInfo::GetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWindowsUpdateAgentInfo.GetInfo
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWindowsUpdateAgentInfo::GetInfo


## -description


Retrieves version information about Windows Update Agent (WUA).


## -parameters




### -param varInfoIdentifier [in]

 A literal string value that specifies  the type of information  that  the <i>retval</i> parameter returns. The following table lists the current possible string values.

<table>
<tr>
<td><b>ApiMajorVersion</b></td>
<td>Retrieves the current major version of WUA.</td>
</tr>
<tr>
<td><b>ApiMinorVersion</b></td>
<td>Retrieves the current minor version of WUA.</td>
</tr>
<tr>
<td><b>ProductVersionString</b></td>
<td>Retrieves  the file version of the Wuapi.dll file in string format.</td>
</tr>
</table>
 


### -param retval [out]

<ul>
<li>Returns the major version of the WUA API as a <b>LONG</b> value  within the  <b>VARIANT</b> variable if the value of the <i>varInfoIdentifier</i> parameter is <b>ApiMajorVersion</b>.</li>
<li>Returns the minor version of the WUA API as a <b>LONG</b> value within the  <b>VARIANT</b> variable if the value of <i>varInfoIdentifier</i> is <b>ApiMinorVersion</b>.</li>
<li>Returns the file version of the Wuapi.dll file  as a <b>BSTR</b> value within the  <b>VARIANT</b> variable if the value of <i>varInfoIdentifier</i> is <b>ProductVersionString</b>.</li>
</ul>
<div class="alert"><b>Note</b>  The format of a returned string is as follows:  "<i>&lt;Windows-major-version&gt;</i>.<i>&lt;Windows-minor-version&gt;</i>.<i>&lt;build&gt;</i>.<i>&lt;update&gt;</i>".</div>
<div> </div>

## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.




## -remarks



The <a href="https://msdn.microsoft.com/46692b86-0fd9-4e48-9fb2-0ea3521b6bca">IWindowsUpdateAgentInfo</a> interface  may require you to update WUA. For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.

The major version is incremented one time for each release if a change occurs in the interfaces of the WUA API. The minor version is incremented one time for each release if a change occurs in the existing interfaces of the WUA API.




## -see-also




<a href="https://msdn.microsoft.com/46692b86-0fd9-4e48-9fb2-0ea3521b6bca">IWindowsUpdateAgentInfo</a>
 

 

