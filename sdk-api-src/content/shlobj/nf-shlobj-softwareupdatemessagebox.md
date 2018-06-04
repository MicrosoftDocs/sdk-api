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

# SoftwareUpdateMessageBox function


## -description


Displays a standard message box that can be used to notify a user that an application has been updated.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window.


### -param pszDistUnit [in]

Type: <b>PCWSTR</b>

The string value containing the identifier for the code distribution unit. For ActiveX controls, <i>pszDistUnit</i> is typically a GUID.


### -param dwFlags

Type: <b>DWORD</b>

Reserved. Must be set to zero.


### -param psdi [out, optional]

Type: <b>LPSOFTDISTINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/e113967a-e52c-41d7-961a-2c305790543e">SOFTDISTINFO</a> structure that, when this method returns successfully, receives the update information. The <b>cbSize</b> member must be initialized to the <code>sizeof(SOFTDISTINFO)</code>.


## -returns



Type: <b>DWORD</b>

Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDNO</b></dt>
</dl>
</td>
<td width="60%">
The user clicked the <b>Do Not Update</b> button on the dialog box.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDYES</b></dt>
</dl>
</td>
<td width="60%">
The user clicked the <b>Update Now</b> or <b>About Update</b> button. The application should navigate to the HTML page referred to by the <b>szHREF</b> member of the structure pointed to by <i>psdi</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDIGNORE</b></dt>
</dl>
</td>
<td width="60%">
There is no pending software update.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IDABORT</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>
 




## -remarks



The preferred way to handle updates is to author a Channel Definition Format (CDF) with an Open Software Description (OSD) vocabulary and make the shortcut OSD-aware. Refer to the <a href="_inet_Active_Channel_Technology_Overview">Channel Definition Format</a> documentation for details.

The <b>SoftwareUpdateMessageBox</b> function is intended to be used in the case where Shell shortcut hooks do not work. One example is an application that was not installed on the start menu. If that application needs to do its own software update check, it should use this function.



