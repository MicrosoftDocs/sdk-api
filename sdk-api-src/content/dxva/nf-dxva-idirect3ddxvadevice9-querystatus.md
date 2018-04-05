---
UID: NF:dxva.IDirect3DDXVADevice9.QueryStatus
title: IDirect3DDXVADevice9::QueryStatus method
author: windows-driver-content
description: Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.
old-location: mf\idirect3ddxvadevice9_querystatus.htm
old-project: medfound
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 0x00, 0x01, IDirect3DDXVADevice9, IDirect3DDXVADevice9 interface [Media Foundation], QueryStatus method, IDirect3DDXVADevice9::QueryStatus, QueryStatus method [Media Foundation], QueryStatus method [Media Foundation], IDirect3DDXVADevice9 interface, QueryStatus,IDirect3DDXVADevice9.QueryStatus, dxva/IDirect3DDXVADevice9::QueryStatus, mf.idirect3ddxvadevice9_querystatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: COPP_TVProtectionStandard
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva.h
api_name:
-	IDirect3DDXVADevice9.QueryStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirect3DDXVADevice9::QueryStatus method


## -description


Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.
      


## -parameters




### -param pSurface

Pointer to the <b>IDirect3DSurface9</b> interface of the surface to query.


### -param Flags


            Specifies the type of query to perform.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0x00"></a><a id="0X00"></a><dl>
<dt><b>0x00</b></dt>
</dl>
</td>
<td width="60%">
Test whether the surface is safe to use for writing.

</td>
</tr>
<tr>
<td width="40%"><a id="0x01"></a><a id="0X01"></a><dl>
<dt><b>0x01</b></dt>
</dl>
</td>
<td width="60%">
Test whether the surface is safe to use for reading.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/63f77cf9-4c04-4ddb-9582-cfcf86f66a2a">IDirect3DDXVADevice9</a>
 

 

