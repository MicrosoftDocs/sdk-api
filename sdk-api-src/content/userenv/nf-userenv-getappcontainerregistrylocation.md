---
UID: NF:userenv.GetAppContainerRegistryLocation
title: GetAppContainerRegistryLocation function
author: windows-driver-content
description: Gets the location of the registry storage associated with an app container.
old-location: shell\getappcontainerregistrylocation.htm
old-project: shell
ms.assetid: DAD7EC07-D57D-40F5-AA99-AD7579910294
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetAppContainerRegistryLocation, GetAppContainerRegistryLocation function [Windows Shell], shell.getappcontainerregistrylocation, userenv/GetAppContainerRegistryLocation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	GetAppContainerRegistryLocation
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# GetAppContainerRegistryLocation function


## -description


Gets the location of the registry storage associated with an app container.


## -parameters




### -param desiredAccess [in]

Type: <b><a href="https://msdn.microsoft.com/003f6be9-e4ba-4d23-b486-a167063c630e">REGSAM</a></b>

The desired registry access.


### -param phAppContainerKey [out]

Type: <b>PHKEY</b>

A pointer to an HKEY that, when this function returns successfully, receives the registry storage location for the current profile.


## -returns



Type: <b>HRESULT</b>

This function returns an <b>HRESULT</b> code, including but not limited to the following:

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The caller is not running as or impersonating a user who can access this profile.

</td>
</tr>
</table>
 




## -remarks



The function gets the registry storage for the current user. To get the registry storage for another user, you must impersonate that user.




## -see-also




<a href="https://msdn.microsoft.com/7D3AB78D-C094-4F89-8032-13F3C137E910">GetAppContainerFolderPath</a>
 

 

