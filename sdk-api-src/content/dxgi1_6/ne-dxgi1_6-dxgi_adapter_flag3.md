---
UID: NE:dxgi1_6.DXGI_ADAPTER_FLAG3
title: DXGI_ADAPTER_FLAG3
author: windows-sdk-content
description: Identifies the type of DXGI adapter.
old-location: direct3ddxgi\DXGI_ADAPTER_FLAG3.htm
old-project: direct3ddxgi
ms.assetid: 3CD83EEB-2F13-4B32-9E27-CF8456FB3E39
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: DXGI_ADAPTER_FLAG3, DXGI_ADAPTER_FLAG3 enumeration [DXGI], DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE, DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE, DXGI_ADAPTER_FLAG3_NONE, DXGI_ADAPTER_FLAG3_REMOTE, DXGI_ADAPTER_FLAG3_SOFTWARE, DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES, DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES, DXGI_ADAPTER_FLAG_FORCE_DWORD, direct3ddxgi.DXGI_ADAPTER_FLAG3, dxgi1_6/DXGI_ADAPTER_FLAG3, dxgi1_6/DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE, dxgi1_6/DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE, dxgi1_6/DXGI_ADAPTER_FLAG3_NONE, dxgi1_6/DXGI_ADAPTER_FLAG3_REMOTE, dxgi1_6/DXGI_ADAPTER_FLAG3_SOFTWARE, dxgi1_6/DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES, dxgi1_6/DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES, dxgi1_6/DXGI_ADAPTER_FLAG_FORCE_DWORD
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgi1_6.h
req.include-header: 
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
req.typenames: DXGI_ADAPTER_FLAG3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_6.h
api_name:
 - DXGI_ADAPTER_FLAG3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_ADAPTER_FLAG3 enumeration


## -description


Identifies the type of DXGI adapter.


## -enum-fields




### -field DXGI_ADAPTER_FLAG3_NONE

Specifies no flags.


### -field DXGI_ADAPTER_FLAG3_REMOTE

Value always set to 0. This flag is reserved.


### -field DXGI_ADAPTER_FLAG3_SOFTWARE

Specifies a software adapter. For more info about this flag, see <a href="https://msdn.microsoft.com/library/Bb205075(v=VS.85).aspx">new info in Windows 8 about enumerating adapters</a>.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.


### -field DXGI_ADAPTER_FLAG3_ACG_COMPATIBLE

Specifies that the adapter's driver has been confirmed to work in an OS process where Arbitrary Code Guard (ACG) is enabled (i.e. dynamic code generation is disallowed).


### -field DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES

Specifies that the adapter supports monitored fences. These adapters support the <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device::CreateFence</a> and <a href="https://msdn.microsoft.com/C077BAD4-08D2-4F1F-8313-5066F68F014C">ID3D11Device5::CreateFence</a> functions.


### -field DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES

Specifies that the adapter supports non-monitored fences. These adapters support the <a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device::CreateFence</a> function together with the <a href="https://msdn.microsoft.com/EF725566-B77A-40EE-B5E3-86C5D13CC7D5">D3D12_FENCE_FLAG_NON_MONITORED</a> flag.

<div class="alert"><b>Note</b>  For adapters that support both monitored and non-monitored fences, non-monitored fences are only supported when created with the <a href="https://msdn.microsoft.com/EF725566-B77A-40EE-B5E3-86C5D13CC7D5">D3D12_FENCE_FLAG_SHARED</a> and <b>D3D12_FENCE_FLAG_SHARED_CROSS_ADAPTER</b> flags. Monitored fences should always be used by supporting adapters unless communicating with an adapter that only supports non-monitored fences.</div>
<div> </div>

### -field DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE

Specifies that the adapter claims keyed mutex conformance. This signals a stronger guarantee that the <a href="https://msdn.microsoft.com/f790eb46-f116-4258-8c8d-de1ece4a1f21">IDXGIKeyedMutex</a> interface behaves correctly.


### -field DXGI_ADAPTER_FLAG3_FORCE_DWORD




#### - DXGI_ADAPTER_FLAG_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile 
            to a size other than 32 bits. This value is not used.


## -remarks



The <b>DXGI_ADAPTER_FLAG3</b> enumerated type is used by the <b>Flags</b> member of the <a href="https://msdn.microsoft.com/A04B37C9-9F83-4812-AAF6-14FA49976051">DXGI_ADAPTER_DESC3</a> structure to ientify the type of DXGI adapter.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

