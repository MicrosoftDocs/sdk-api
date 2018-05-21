---
UID: NF:ras.RasSetEapUserDataA
title: RasSetEapUserDataA function
author: windows-driver-content
description: Use the RasSetEapUserData function to store user-specific Extensible Authentication Protocol (EAP) information for the specified phone-book entry in the registry.
old-location: rras\rasseteapuserdata.htm
old-project: RRAS
ms.assetid: 702e5c42-cc8c-43cf-a0bf-d3e450c031a4
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: RasSetEapUserData, RasSetEapUserData function [RAS], RasSetEapUserDataA, RasSetEapUserDataW, _ras_rasseteapuserdata, ras/RasSetEapUserData, ras/RasSetEapUserDataA, ras/RasSetEapUserDataW, rras.rasseteapuserdata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasSetEapUserDataW (Unicode) and RasSetEapUserDataA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rasapi32.dll
api_name:
-	RasSetEapUserData
-	RasSetEapUserDataA
-	RasSetEapUserDataW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RasSetEapUserDataA function


## -description


Use the 
<b>RasSetEapUserData</b> function to store user-specific Extensible Authentication Protocol (EAP) information for the specified phone-book entry in the registry.


## -parameters




### -param hToken [in]

Handle to a primary or impersonation access token that represents the user for which to store data. This parameter can be <b>NULL</b> if the function is called from a process already running in the user's context.


### -param pszPhonebook [in]

Pointer to a <b>null</b>-terminated string that specifies the full path of the phone-book (PBK) file. If this parameter is <b>NULL</b>, the function  uses the system phone book.


### -param pszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies an existing entry name.


### -param pbEapData [in]

Pointer to the data to store for the user.


### -param dwSizeofEapData [in]

Specifies the size of the data pointed to by the <i>pbEapData</i> parameter.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSizeofEapData</i> parameter is zero, or the <i>pbEapData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_OPEN_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
<b>RasSetEapUserData</b> was unable to open the specified phone-book file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
<b>RasSetEapUserData</b> was unable to find the specified entry in the phone book.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6b1a1c73-28af-43ff-b79c-c796ddae219c">RasGetEapUserData</a>



<a href="https://msdn.microsoft.com/60661c23-3d6a-4b0c-9cc9-bf04ecea2425">RasInvokeEapUI</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

