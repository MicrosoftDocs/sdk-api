---
UID: NF:d3d9helper.IDirect3D9.GetAdapterIdentifier
title: IDirect3D9::GetAdapterIdentifier
author: windows-sdk-content
description: Describes the physical display adapters present in the system when the IDirect3D9 interface was instantiated.
old-location: direct3d9\idirect3d9__getadapteridentifier.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9__getadapteridentifier.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetAdapterIdentifier, GetAdapterIdentifier method [Direct3D 9], GetAdapterIdentifier method [Direct3D 9],IDirect3D9 interface, IDirect3D9 interface [Direct3D 9],GetAdapterIdentifier method, IDirect3D9.GetAdapterIdentifier, IDirect3D9::GetAdapterIdentifier, ab3a7dce-1e55-5674-03b7-13a53540bbf5, d3d9helper/IDirect3D9::GetAdapterIdentifier, direct3d9.idirect3d9__getadapteridentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9helper.h
req.include-header: D3D9.h
req.redist: 
req.target-type: Windows
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9.GetAdapterIdentifier
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9::GetAdapterIdentifier


## -description


Describes the physical display adapters present in the system when the <a href="https://msdn.microsoft.com/en-us/library/Bb174300(v=VS.85).aspx">IDirect3D9</a> interface was instantiated.


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number that denotes the display adapter. D3DADAPTER_DEFAULT is always the primary display adapter. The minimum value for this parameter is 0, and the maximum value for this parameter is one less than the value returned by <a href="https://msdn.microsoft.com/en-us/library/Bb174315(v=VS.85).aspx">GetAdapterCount</a>. 


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flags sets the <b>WHQLLevel</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb172505(v=VS.85).aspx">D3DADAPTER_IDENTIFIER9</a>. Flags can be set to either 0 or D3DENUM_WHQL_LEVEL. If D3DENUM_WHQL_LEVEL is specified, this call can connect to the Internet to download new Microsoft Windows Hardware Quality Labs (WHQL) certificates.

Differences between Direct3D 9 and Direct3D 9Ex:

D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system). Any of these operating systems return 1 in the <b>WHQLLevel</b> member of <a href="https://msdn.microsoft.com/en-us/library/Bb172505(v=VS.85).aspx">D3DADAPTER_IDENTIFIER9</a> without checking the status of the driver. 


### -param pIdentifier [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172505(v=VS.85).aspx">D3DADAPTER_IDENTIFIER9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb172505(v=VS.85).aspx">D3DADAPTER_IDENTIFIER9</a> structure to be filled with information describing this adapter. If <i>Adapter</i> is greater than or equal to the number of adapters in the system, this structure will be zeroed. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if Adapter is out of range, if Flags contains unrecognized parameters, or if pIdentifier is <b>NULL</b> or points to unwriteable memory.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174315(v=VS.85).aspx">GetAdapterCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174300(v=VS.85).aspx">IDirect3D9</a>
 

 

