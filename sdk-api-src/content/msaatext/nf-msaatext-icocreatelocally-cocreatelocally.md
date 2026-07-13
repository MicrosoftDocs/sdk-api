---
UID: NF:msaatext.ICoCreateLocally.CoCreateLocally
title: ICoCreateLocally::CoCreateLocally (msaatext.h)
description: Clients call ICoCreateLocally::CoCreateLocally to create a helper object in the same context as the server object.
helpviewer_keywords: ["CoCreateLocally","CoCreateLocally method [Windows Accessibility]","CoCreateLocally method [Windows Accessibility]","ICoCreateLocally interface","ICoCreateLocally interface [Windows Accessibility]","CoCreateLocally method","ICoCreateLocally.CoCreateLocally","ICoCreateLocally::CoCreateLocally","_msaa_ICoCreateLocally_CoCreateLocally","msaa.icocreatelocally_icocreatelocally__cocreatelocally","msaatext/ICoCreateLocally::CoCreateLocally","winauto.icocreatelocally_icocreatelocally__cocreatelocally"]
old-location: winauto\icocreatelocally_icocreatelocally__cocreatelocally.htm
tech.root: WinAuto
ms.assetid: 3a41dd9d-71b3-4d7c-9728-a65f7ddac3d5
ms.date: 12/05/2018
ms.keywords: CoCreateLocally, CoCreateLocally method [Windows Accessibility], CoCreateLocally method [Windows Accessibility],ICoCreateLocally interface, ICoCreateLocally interface [Windows Accessibility],CoCreateLocally method, ICoCreateLocally.CoCreateLocally, ICoCreateLocally::CoCreateLocally, _msaa_ICoCreateLocally_CoCreateLocally, msaa.icocreatelocally_icocreatelocally__cocreatelocally, msaatext/ICoCreateLocally::CoCreateLocally, winauto.icocreatelocally_icocreatelocally__cocreatelocally
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
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - ICoCreateLocally::CoCreateLocally
 - msaatext/ICoCreateLocally::CoCreateLocally
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - ICoCreateLocally.CoCreateLocally
---

# ICoCreateLocally::CoCreateLocally


## -description

Clients call <b>ICoCreateLocally::CoCreateLocally</b> to create a helper object in the same context as the server object. This allows clients to increase performance because they are running in the server application.<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div>
<div> </div>

## -parameters

### -param rclsid [in]

Type: <b>REFCLSID</b>

Class identifier of the object to be created locally.

### -param dwClsContext [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

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