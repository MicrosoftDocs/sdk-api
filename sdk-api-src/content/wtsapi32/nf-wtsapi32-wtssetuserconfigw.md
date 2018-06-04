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

# WTSSetUserConfigW function


## -description


Modifies configuration information for the specified user on the specified domain controller or 
    Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param pServerName [in]

Pointer to a null-terminated string containing the name of a domain controller or 
      RD Session Host server. Specify <b>WTS_CURRENT_SERVER_NAME</b> to indicate the 
      RD Session Host server on which your application is running.


### -param pUserName [in]

Pointer to a null-terminated string containing the name of the user whose configuration is being set.


### -param WTSConfigClass [in]

Specifies the type of information to set for the user. This parameter can be one of the values from the 
      <a href="https://msdn.microsoft.com/623b8a86-aa0d-497c-a2e6-5526f9b13d98">WTS_CONFIG_CLASS</a> enumeration type. The 
      documentation for <b>WTS_CONFIG_CLASS</b> describes 
      the format of the data specified in <i>ppBuffer</i> for each of the information types.


### -param pBuffer [in]

Pointer to the data used to modify the specified user's configuration.


### -param DataLength [in]

Size, in <b>TCHARs</b>, of the <i>pBuffer</i> buffer.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/aabbcc03-3241-49ab-ab11-ccd3e6893e78">WTSQueryUserConfig</a> and 
    <b>WTSSetUserConfig</b> functions are passed a server 
    name instead of a handle because user account information often resides on a domain controller. To set user 
    configuration information, use the primary domain controller. You can call the 
    <a href="https://msdn.microsoft.com/3e32aacc-088e-455a-bc1b-92274e98d2e5">NetGetDCName</a> function to get the name of the primary 
    domain controller. To query user configuration information, you can use the 
    <a href="https://msdn.microsoft.com/64dacbf4-46c2-4f82-b250-b7d338535e7c">NetGetAnyDCName</a> function to get the name of a 
    primary or backup domain controller.

Any domain controller can set or query user configuration information. Use the 
    <a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> function to retrieve the name of a domain 
    controller.

If the value of the  <i>WTSConfigClass</i> parameter corresponds to an integer value in the 
     <a href="https://msdn.microsoft.com/623b8a86-aa0d-497c-a2e6-5526f9b13d98">WTS_CONFIG_CLASS</a> enumeration, define the value 
     to be set as a <b>DWORD</b>.  Then cast the value to an <b>LPWSTR</b> 
     in the call to <b>WTSSetUserConfig</b>, as in the 
     following example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WTSSetUserConfig( strServer.GetBuffer(0), 
                  m_strName.GetBuffer(0), 
                  WTSUserConfigfAllowLogonTerminalServer, 
                  (LPWSTR) &amp;dwEnable, 
                  sizeof(DWORD));</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/aabbcc03-3241-49ab-ab11-ccd3e6893e78">WTSQueryUserConfig</a>



<a href="https://msdn.microsoft.com/623b8a86-aa0d-497c-a2e6-5526f9b13d98">WTS_CONFIG_CLASS</a>
 

 

