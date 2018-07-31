---
UID: NF:wpcapi.IWindowsParentalControlsCore.GetUserSettings
title: IWindowsParentalControlsCore::GetUserSettings
author: windows-sdk-content
description: Retrieves a pointer to an interface for general settings for the specified user.
old-location: parcon\iwindowsparentalcontrols_getusersettings.htm
old-project: parcon
ms.assetid: 92c7a138-10b8-4bdf-afea-985e203e04e4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetUserSettings, GetUserSettings method, GetUserSettings method,IWindowsParentalControlsCore interface, IWindowsParentalControlsCore interface,GetUserSettings method, IWindowsParentalControlsCore.GetUserSettings, IWindowsParentalControlsCore::GetUserSettings, parcon.iwindowsparentalcontrols_getusersettings, wpcapi/IWindowsParentalControlsCore::GetUserSettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wpcapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wpcapi.h
api_name:
 - IWindowsParentalControlsCore.GetUserSettings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWindowsParentalControlsCore::GetUserSettings


## -description


Retrieves a pointer to an interface for general settings for the specified user.


## -parameters




### -param pcszSID [in]

The SID string of the user. If this parameter is <b>NULL</b>, retrieve settings for the current user.


### -param ppSettings [out]

A pointer to an <a href="https://msdn.microsoft.com/92ae8611-fbb4-470e-8a48-395defaef904">IWPCSettings</a> interface pointer.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The user settings were not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f825388f-c4de-4bf2-8076-6efd81b6e030">IWindowsParentalControls</a>



<a href="parcon.iwindowsparentalcontrolscore">IWindowsParentalControlsCore</a>
 

 

