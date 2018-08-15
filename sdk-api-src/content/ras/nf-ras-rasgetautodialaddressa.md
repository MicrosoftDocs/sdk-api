---
UID: NF:ras.RasGetAutodialAddressA
title: RasGetAutodialAddressA function
author: windows-sdk-content
description: The RasGetAutodialAddress function retrieves information about all the AutoDial entries associated with a network address in the AutoDial mapping database.
old-location: rras\rasgetautodialaddress.htm
old-project: rras
ms.assetid: b7182760-30c0-4c09-ae99-f656d868e150
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RasGetAutodialAddress, RasGetAutodialAddress function [RAS], RasGetAutodialAddressA, RasGetAutodialAddressW, _ras_rasgetautodialaddress, ras/RasGetAutodialAddress, ras/RasGetAutodialAddressA, ras/RasGetAutodialAddressW, rras.rasgetautodialaddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ras.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetAutodialAddressW (Unicode) and RasGetAutodialAddressA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasGetAutodialAddress
 - RasGetAutodialAddressA
 - RasGetAutodialAddressW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: ADAM
---

# RasGetAutodialAddressA function


## -description


The 
<b>RasGetAutodialAddress</b> function retrieves information about all the AutoDial entries associated with a network address in the AutoDial mapping database.


## -parameters




### -param

TBD




#### - [in]

Pointer to a <b>null</b>-terminated string that specifies the address for which information is requested. This can be an IP address, Internet host name ("www.microsoft.com"), or NetBIOS name ("products1").

If this parameter is <b>NULL</b>, the function retrieves the default Internet connection. The function returns the per-user default Internet connection if one is configured. Otherwise, the function returns the global default Internet connection. If no default Internet connections are configured, the function returns zero for the <i>lpdwcbAutoDialEntries</i> and <i>lpdwcAutoDialEntries</i> parameters.


#### - lpAutoDialEntries [in, out]

Pointer to a buffer that, on output, receives an array of 
<a href="https://msdn.microsoft.com/a62a1e86-a433-44dd-8068-cb4d60b124c3">RASAUTODIALENTRY</a> structures, one for each AutoDial entry associated with the address specified by the <i>lpszAddress</i> parameter. 




On input, set the <b>dwSize</b> member of the first 
<a href="https://msdn.microsoft.com/a62a1e86-a433-44dd-8068-cb4d60b124c3">RASAUTODIALENTRY</a> structure in the buffer to sizeof(RASAUTODIALENTRY) to identify the version of the structure.

If <i>lpAutoDialEntries</i> is <b>NULL</b>, 
<b>RasGetAutodialAddress</b> sets the <i>lpdwcbAutoDialEntries</i> and <i>lpdwcAutoDialEntries</i> parameters to indicate the required buffer size, in bytes, and the number of AutoDial entries.


#### - lpdwReserved [in]

Reserved; must be <b>NULL</b>.


#### - lpdwcAutoDialEntries [out]

Pointer to a variable that receives the number of structure elements returned in the <i>lpAutoDialEntries</i> buffer.


#### - lpdwcbAutoDialEntries [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the <i>lpAutoDialEntries</i> buffer. 




On output, this variable receives the number of bytes returned, or the number of bytes required if the buffer is too small.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the 
<a href="https://msdn.microsoft.com/a62a1e86-a433-44dd-8068-cb4d60b124c3">RASAUTODIALENTRY</a> structure is an invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszAddress</i>, <i>lpdwcbAutoDialEntries</i>, or <i>lpdwcAutoDialEntries</i> parameter was <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The Remote Access Service (RAS) supports default Internet connections. RAS supports a default Internet connection that is global to the local computer, and in addition, supports a default Internet connection for each user.

The name of the global default Internet connection is stored in the registry below the following registry key:


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Ras Autodial</b>
            <b>Default</b></pre>


The value that stores the name of the connection is: 
			

<b>DefaultInternet</b>

This value is of type <b>REG_SZ</b>.

The global default Internet connection must be configured as a <b>For all users</b> connection in the <b>Connections Folder</b> user interface.

The name of the per-user default Internet connection is stored in the registry below the following registry key: 
			


<b>HKEY_CURRENT_USER</b>\<b>Software</b>\<b>Microsoft</b>\<b>Ras Autodial</b>\<b>Default</b>



The value that stores the name of the connection is: 
			

<b>DefaultInternet</b>

This value is of type <b>REG_SZ</b>.




## -see-also




<a href="https://msdn.microsoft.com/a62a1e86-a433-44dd-8068-cb4d60b124c3">RASAUTODIALENTRY</a>



<a href="https://msdn.microsoft.com/bd4fb897-5cc0-452f-b6a2-ec0540c59b90">RasEnumAutodialAddresses</a>



<a href="https://msdn.microsoft.com/267d4f8e-0e0b-4636-8f30-3c39bbb8d4e9">RasSetAutodialAddress</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

