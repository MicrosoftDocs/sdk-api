---
UID: NF:bits3_0.IBitsPeerCacheAdministration.EnumPeers
title: IBitsPeerCacheAdministration::EnumPeers
author: windows-sdk-content
description: Gets an IEnumBitsPeers interface pointer that you use to enumerate the peers that can serve content. The enumeration is a snapshot of the records in the cache.
old-location: bits\ibitspeercacheadministration_enumpeers.htm
old-project: bits
ms.assetid: 8786d7d8-9ffb-4492-9834-90b97f97e4cf
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EnumPeers, EnumPeers method [BITS], EnumPeers method [BITS],IBitsPeerCacheAdministration interface, IBitsPeerCacheAdministration interface [BITS],EnumPeers method, IBitsPeerCacheAdministration.EnumPeers, IBitsPeerCacheAdministration::EnumPeers, bits.ibitspeercacheadministration_enumpeers, bits3_0/IBitsPeerCacheAdministration::EnumPeers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_CERT_STORE_LOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration.EnumPeers
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: 
req.irql: 
---

# IBitsPeerCacheAdministration::EnumPeers


## -description


Gets an <a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. The enumeration is a snapshot of the records in the cache.


## -parameters




### -param ppEnum [out]

An <a href="https://msdn.microsoft.com/2715a58c-ba76-4223-ad9e-453d029e0eda">IEnumBitsPeers</a> interface pointer that you use to enumerate the peers that can serve content. Release <i>ppEnum</i> when done.


## -returns



This method returns S_OK on success or one of the standard COM <b>HRESULT</b> values on error.




## -see-also




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/79a739ed-7618-410a-a6df-fab11794d932">IBitsPeerCacheAdministration::ClearPeers</a>



<a href="https://msdn.microsoft.com/c83632c2-5d01-48ab-93ef-961778c2379a">IBitsPeerCacheAdministration::DiscoverPeers</a>
 

 

