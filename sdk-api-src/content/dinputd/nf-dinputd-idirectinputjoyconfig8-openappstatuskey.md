---
UID: NF:dinputd.IDirectInputJoyConfig8.OpenAppStatusKey
title: IDirectInputJoyConfig8::OpenAppStatusKey
author: windows-sdk-content
description: The IDirectInputJoyConfig8::OpenAppStatusKey method opens the root key of the application status registry keys, and obtains a handle to the key as a return parameter.
old-location: hid\idirectinputjoyconfig8_openappstatuskey.htm
old-project: hid
ms.assetid: a9caea40-6570-4756-81a4-91a3aaff302b
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: IDirectInputJoyConfig8 interface [Human Input Devices],OpenAppStatusKey method, IDirectInputJoyConfig8.OpenAppStatusKey, IDirectInputJoyConfig8::OpenAppStatusKey, OpenAppStatusKey, OpenAppStatusKey method [Human Input Devices], OpenAppStatusKey method [Human Input Devices],IDirectInputJoyConfig8 interface, di_ref_004ec952-e0fd-4e41-a466-a09fb37e6f80.xml, dinputd/IDirectInputJoyConfig8::OpenAppStatusKey, hid.idirectinputjoyconfig8_openappstatuskey
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dinputd.h
req.include-header: Dinputd.h
req.target-type: Desktop
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
tech.root: 
req.typenames: DIEFFESCAPE, *LPDIEFFESCAPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dinputd.h
api_name:
 - IDirectInputJoyConfig8.OpenAppStatusKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectInputJoyConfig8::OpenAppStatusKey


## -description


The <b>IDirectInputJoyConfig8::OpenAppStatusKey </b>method opens the root key of the application status registry keys, and obtains a handle to the key as a return parameter. 


## -parameters






#### - phKey

Points to the address of a variable (of type HKEY) that will contain a registry key handle if the method succeeds. See Remarks for additional usage details.


## -returns



Returns DI_OK if successful; otherwise, returns one of the following COM error values. The following error codes are intended to be illustrative and not necessarily comprehensive.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The key is missing on this system. Applications should proceed as if the key were empty. 

</td>
</tr>
</table>
 




## -remarks



The registry key handle returned in the <i>phKey</i> parameter can be used with the standard Win32 registry functions. The Dinputd.h header file defines the following string constants for use in accessing subkeys and named values contained by the application status root key.





