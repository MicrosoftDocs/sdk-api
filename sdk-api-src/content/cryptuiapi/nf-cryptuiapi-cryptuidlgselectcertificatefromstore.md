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

# CryptUIDlgSelectCertificateFromStore function


## -description


The <b>CryptUIDlgSelectCertificateFromStore</b> function displays a dialog box that allows the selection of a certificate from a specified store.


## -parameters




### -param hCertStore [in]

Handle of the certificate store to be searched.


### -param hwnd [in]

Handle of the window for the display. If <b>NULL</b>, defaults to the desktop window.


### -param pwszTitle [in, optional]

String used as the title of the dialog box. If <b>NULL</b>, the default title, "Select Certificate," is used.


### -param pwszDisplayString [in, optional]

Text statement in the selection dialog box. If <b>NULL</b>, the default phrase, "Select a certificate you want to use," is used.


### -param dwDontUseColumn [in]

Flags that can be combined to exclude columns of the display. 



					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></a><a id="cryptui_select_issuedto_column"></a><dl>
<dt><b>CRYPTUI_SELECT_ISSUEDTO_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display the ISSUEDTO information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></a><a id="cryptui_select_issuedby_column"></a><dl>
<dt><b>CRYPTUI_SELECT_ISSUEDBY_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display the ISSUEDBY information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></a><a id="cryptui_select_intendeduse_column"></a><dl>
<dt><b>CRYPTUI_SELECT_INTENDEDUSE_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display IntendedUse information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></a><a id="cryptui_select_friendlyname_column"></a><dl>
<dt><b>CRYPTUI_SELECT_FRIENDLYNAME_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display the display name information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_LOCATION_COLUMN"></a><a id="cryptui_select_location_column"></a><dl>
<dt><b>CRYPTUI_SELECT_LOCATION_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display location information.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></a><a id="cryptui_select_expiration_column"></a><dl>
<dt><b>CRYPTUI_SELECT_EXPIRATION_COLUMN</b></dt>
</dl>
</td>
<td width="60%">
Do not display expiration information.

</td>
</tr>
</table>
 


### -param dwFlags [in]

Currently not used and should be set to 0.


### -param pvReserved [in]

Reserved for future use.


## -returns



Returns a pointer to the selected certificate context. If no certificate was selected, <b>NULL</b> is returned. When you have finished using the certificate, free the certificate context by calling the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d4b8f01b-7c3e-4286-bc37-d5ec4a1e1c2f">CryptUIDlgViewContext</a>
 

 

