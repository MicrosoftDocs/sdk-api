---
UID: NF:ras.RasGetEntryPropertiesW
title: RasGetEntryPropertiesW function
author: windows-sdk-content
description: The RasGetEntryProperties function retrieves the properties of a phone-book entry.
old-location: rras\rasgetentryproperties.htm
tech.root: rras
ms.assetid: eef9c197-04b3-4f3c-a7bd-8c62f9fac560
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: RasGetEntryProperties, RasGetEntryProperties function [RAS], RasGetEntryPropertiesA, RasGetEntryPropertiesW, _ras_rasgetentryproperties, ras/RasGetEntryProperties, ras/RasGetEntryPropertiesA, ras/RasGetEntryPropertiesW, rras.rasgetentryproperties
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
req.unicode-ansi: RasGetEntryPropertiesW (Unicode) and RasGetEntryPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
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
 - RasGetEntryProperties
 - RasGetEntryPropertiesA
 - RasGetEntryPropertiesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasGetEntryPropertiesW function


## -description


The 
<b>RasGetEntryProperties</b> function retrieves the properties of a phone-book entry.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD


### -param arg4

TBD


### -param arg5

TBD


### -param arg6

TBD




#### - [in]

Pointer to a <b>null</b>-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. The default phone-book file is the one selected by the user in the <b>User Preferences</b> property sheet of the <b>Dial-Up Networking</b> dialog box. 




<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.


#### - lpRasEntry [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a> structure followed by additional bytes for the alternate phone number list, if there is one. 




On output, the structure receives the connection data associated with the phone-book entry specified by the <i>lpszEntry</i> parameter.

On input, set the <b>dwSize</b> member of the structure to sizeof(<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>) to identify the version of the structure.

This parameter can be <b>NULL</b>.

<b>Windows Me/98 and Windows 95 OSR2:  </b>The 
Microsoft Layer for Unicode does not support <b>dwAlternateOffset</b> in 
<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>.


#### - lpbDeviceInfo [out]

This parameter is no longer used. The calling function should set this parameter to <b>NULL</b>.

<b>Windows Me/98/95:  </b>Pointer to a buffer that receives device-specific configuration information. Do not directly manipulate this opaque TAPI device information. For more information about TAPI device configuration, see the 
<a href="_tapi2_linegetdevconfig">lineGetDevConfig</a> function in the TAPI Programmer's Reference in the Platform SDK. 


This parameter can be <b>NULL</b>.




#### - lpdwDeviceInfoSize [in, out]

This parameter is unused. The calling function should set this parameter to <b>NULL</b>.
						

<b>Windows Me/98/95:  </b>Pointer to a variable that, on input, specifies the size, in bytes, of the buffer specified by the <i>lpbDeviceInfo</i> parameter. 


On output, this variable receives the number of bytes required.

This parameter can be <b>NULL</b> if the <i>lpbDeviceInfo</i> parameter s <b>NULL</b>.

To determine the required buffer size, call 
<b>RasGetEntryProperties</b> with <i>lpbDeviceInfo</i> set to <b>NULL</b> and <i>*lpdwDeviceInfoSize</i> set to zero. The function returns the required buffer size in <i>*lpdwDeviceInfoSize</i>.




#### - lpdwEntryInfoSize [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the <i>lpRasEntry</i> buffer. 




On output, this variable receives the number of bytes required.

This parameter can be <b>NULL</b> if the <i>lpRasEntry</i> parameter is <b>NULL</b>.

To determine the required buffer size, call 
<b>RasGetEntryProperties</b> with <i>lpRasEntry</i> set to <b>NULL</b> and <i>*lpdwEntryInfoSize</i> set to zero. The function returns the required buffer size in <i>*lpdwEntryInfoSize</i>.


#### - lpszEntry [in]

Pointer to a <b>null</b>-terminated string that specifies an existing entry name. If an empty string is specified, the function returns default values in the buffers pointed to by the <i>lpRasEntry</i> and <i>lpbDeviceInfo</i> parameters.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The function was called with an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The value of the dwSize member of the <i>lpRasEntry</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The address or buffer specified by <i>lpRasEntry</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer size indicated in <i>lpdwEntryInfoSize</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The phone-book entry does not exist, or the phone-book file is corrupted and/or has missing components.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/25c46850-4fb7-47a9-9645-139f0e869559">RASENTRY</a>



<a href="https://msdn.microsoft.com/6532b48b-0d80-4993-800e-c808bb7540d6">RasSetEntryProperties</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

