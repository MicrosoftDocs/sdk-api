---
UID: NF:msaatext.ICoCreateLocally.CoCreateLocally
title: ICoCreateLocally::CoCreateLocally
author: windows-sdk-content
description: Clients call ICoCreateLocally::CoCreateLocally to create a helper object in the same context as the server object.
old-location: winauto\icocreatelocally_icocreatelocally__cocreatelocally.htm
tech.root: WinAuto
ms.assetid: 3a41dd9d-71b3-4d7c-9728-a65f7ddac3d5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoCreateLocally, CoCreateLocally method [Windows Accessibility], CoCreateLocally method [Windows Accessibility],ICoCreateLocally interface, ICoCreateLocally interface [Windows Accessibility],CoCreateLocally method, ICoCreateLocally.CoCreateLocally, ICoCreateLocally::CoCreateLocally, _msaa_ICoCreateLocally_CoCreateLocally, msaa.icocreatelocally_icocreatelocally__cocreatelocally, msaatext/ICoCreateLocally::CoCreateLocally, winauto.icocreatelocally_icocreatelocally__cocreatelocally
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msaatext.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - ICoCreateLocally.CoCreateLocally
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# ICoCreateLocally::CoCreateLocally


## -description


Clients call <b>ICoCreateLocally::CoCreateLocally</b> to create a helper object in the same context as the server object. This allows clients to increase performance because they are running in the server application.<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="https://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		</div>
<div> </div>



## -parameters




### -param rclsid [in]

Type: <b>REFCLSID</b>

Class identifier of the object to be created locally.


### -param dwClsContext [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Context in which the helper object should run. This is usually CLSCTX_INPROC_SERVER.


### -param riid [in]

Type: <b>REFIID</b>

The desired interface identifier (IID).


### -param punk [out]

Type: <b>IUnknown*</b>

Interface pointer to the desired interface identifier (from <i>riid</i>).


### -param riidParam [in]

Type: <b>REFIID</b>

An optional interface parameter that is passed to the new helper object. This parameter specifies an interface identifier.


### -param punkParam [in]

Type: <b>IUnknown*</b>

An optional interface parameter that is passed to the new helper object. This parameter specifies the interface pointer.


### -param varParam [in]

Type: <b>VARIANT</b>

An optional interface parameter that is passed to the new helper object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK.

If not successful, returns the following value or another standard COM error code.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The client does not have sufficient permissions to create this object in the server process.

</td>
</tr>
</table>
 



